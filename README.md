# 4096

Um pequeno clone de [1024](https://play.google.com/store/apps/details?id=com.veewo.a1024), baseado no [2048 de Saming](http://saming.fr/p/2048/) e no [2048 original de Gabriele Cirulli](https://github.com/gabrielecirulli/2048). Inspirado indiretamente por [Threes](https://asherv.com/threes/).

Este repositório é um fork mantido por [ZeFerreira77](https://github.com/ZeFerreira77/4096) com o objetivo de chegar ao **bloco 4096**.

## Sobre

Junta os números e chega ao **bloco 4096!**

Jogo de puzzle simples em grelha 4x4, feito em HTML + CSS + JavaScript puro, sem dependências. Funciona no browser, no desktop e no telemóvel (suporte a setas do teclado e swipe).

- Sem build, sem instalação
- Guarda o melhor score em `localStorage`
- Permite continuar a jogar depois de ganhar

## Como jogar

1. Usa as **setas do teclado** (ou faz swipe no telemóvel) para mover os blocos.
2. Quando dois blocos com o mesmo número se tocam, **fundem-se num só**.
3. Cada fusão soma pontos ao score.
4. Ganhas ao criar o bloco **4096**. Podes continuar depois disso para pontuações ainda maiores.
5. Perdes quando a grelha enche e já não há movimentos possíveis.

Botões:
- **New Game / Try again** — recomeça o jogo
- **Keep going** — continua após a vitória

## Como executar localmente

Este projeto foi clonado de:

```bash
git clone https://github.com/ZeFerreira77/4096
```

Para jogar, basta abrir o `index.html` no browser, ou servir a pasta com um servidor estático:

Opção 1 — Abrir direto:
```
duplo clique em index.html
```

Opção 2 — Servidor local (recomendado):
```bash
# Python 3
python -m http.server 8000
# depois abre http://localhost:8000
```

Opção 3 — VS Code:
```
extensão Live Server -> Open with Live Server
```

Não é preciso compilar nada. Se alterares o SCSS em `style/`, recompila para `main.css` com:

```bash
sass --unix-newlines --watch style/main.scss
```

## Estrutura do projeto

```
4096/
├── index.html          # Página principal do jogo
├── js/                 # Lógica do jogo
│   ├── game_manager.js # Regras, vitória/derrota, score
│   ├── grid.js         # Grelha 4x4
│   ├── tile.js         # Blocos
│   ├── html_actuator.js# Renderização
│   ├── keyboard_input_manager.js # Teclado + swipe
│   ├── local_storage_manager.js  # Best score + save
│   └── application.js  # Arranque
├── style/
│   ├── main.scss       # Fonte — edita este
│   └── main.css        # Gerado — é este que o browser usa
├── meta/               # Ícones Apple touch / splash
├── favicon.ico
├── CONTRIBUTING.md
└── LICENSE.txt (MIT)
```

## Tecnologias

- HTML5
- CSS3 / SCSS
- JavaScript (vanilla, sem framework)
- Web Storage (`localStorage`)

## Créditos / Contribuições originais

Jogo original por [Gabriele Cirulli](http://gabrielecirulli.com), baseado em [1024 by Veewo Studio](https://itunes.apple.com/us/app/1024!/id823499224) e [Threes by Asher Vollmer](http://asherv.com/threes/).

Manutenção do original: [Anna Harren](https://github.com/iirelu/) e [sigod](https://github.com/sigod).

Outros contributos notáveis no upstream:
- [TimPetricola](https://github.com/TimPetricola) — best score
- [chrisprice](https://github.com/chrisprice) — swipe no mobile
- [marcingajda](https://github.com/marcingajda) — swipe no Windows Phone
- [mgarciaisaia](https://github.com/mgarciaisaia) — suporte Android 2.3

Ver [CONTRIBUTING.md](./CONTRIBUTING.md) para contribuir com este fork.

## Licença

Licenciado sob [MIT](./LICENSE.txt). Copyright (c) 2014 Gabriele Cirulli.

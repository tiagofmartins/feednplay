# FeedNPlay

O FeedNPlay é uma parede de ecrãs interativa instalada no corredor de entrada do Departamento de Engenharia Informática da Universidade de Coimbra (DEI-FCTUC). É um meio de comunicação do departamento com a sua comunidade e com quem o visita, e uma tela para mostrar, explorar e experimentar trabalho na interseção entre ciência, tecnologia, arte e design.

```
├───────────── 9720 px ─────────────┤
┌───┬───┬───┬───┬───┬───┬───┬───┬───┐ ┬
│   │   │   │   │   │   │   │   │   │ │
│ 1 │ 2 │ 3 │ 4 │ 5 │ 6 │ 7 │ 8 │ 9 │ 1920 px
│   │   │   │   │   │   │   │   │   │ │
└───┴───┴───┴───┴───┴───┴───┴───┴───┘ ┴
├───┤ 1080 px
```

Este repositório reúne as especificações da parede e um conjunto de exemplos que servem de ponto de partida a quem quiser criar conteúdos para o FeedNPlay.

## O que é

Uma fila de 9 monitores em retrato que formam uma única imagem contínua, controlada por um computador dedicado e equipada com câmaras de vídeo. Está colocada logo a seguir à entrada principal do DEI, num dos corredores mais movimentados do departamento, onde é vista todos os dias por estudantes, investigadores, docentes, funcionários e visitantes.

O conteúdo pode ir de imagens, vídeos e tipografia em movimento a visualizações de informação, arte generativa e instalações interativas que respondem em tempo real a quem passa.

## Para quem

- Estudantes, para mostrar trabalhos de aulas ou dissertações.
- Investigadores, para divulgar ou testar projetos com um público real.
- Docentes, como suporte a aulas e exercícios.
- Artistas, designers e criativos convidados.
- Quem passa no corredor, que vê e interage com o que está a ser mostrado.

## Para que serve

- Mostrar o que se faz no DEI, tanto em ensino como em investigação.
- Divulgar o que acontece no departamento, na cidade e no mundo, como palestras, exposições e eventos.
- Servir de plataforma de experimentação para novos formatos e novas formas de interação com ecrãs de grande escala.
- Criar um ciclo de exposição e criação: o que é mostrado inspira novos trabalhos, que voltam a ser mostrados na parede.

Qualquer pessoa pode propor conteúdos. As propostas passam por um processo de curadoria que avalia a qualidade e a viabilidade de cada trabalho. Periodicamente são lançadas chamadas temáticas, por exemplo arte interativa, animação, tipografia digital ou código generativo.

## Especificações

### Ecrã

- 9 monitores NEC MultiSync UN552VS (55"), em retrato, lado a lado numa fila (9 × 1).
- Resolução por monitor: 1080 × 1920 píxeis.
- Resolução total: 9720 × 1920 píxeis (proporção de aproximadamente 5:1).
- Dimensões físicas da parede: 6,12 × 1,21 m.
- Frequência de atualização: 60 Hz.

### Interação

- Uma câmara a cerca de 6 metros de altura, com uma perspetiva aérea do espaço à frente do FeedNPlay.
- Câmaras na moldura do FeedNPlay, para perspetivas mais frontais.
- Um hub USB atrás dos monitores, que permite ligar outros sensores ou dispositivos ao computador e, através dele, ao conteúdo.

### Computador

- Mac Studio M5.
- O computador liga-se aos 9 monitores através de 3 Matrox QuadHead2Go Q155 HDMI, cada uma a alimentar 3 monitores. Por isso, o computador vê 3 ecrãs de 3240 × 1920, lado a lado, um por cada trio de monitores. Para ocupar a parede toda, a aplicação deve abrir uma única janela sem moldura com 9720 × 1920 que atravesse os 3 ecrãs.

## Criar conteúdos

> [!WARNING]
> Nada pode ficar parado no mesmo sítio. Os monitores sofrem de *burn-in*: um elemento visual que fica fixo na mesma posição durante muito tempo, como texto, um logótipo, um QR code ou uma moldura, pode deixar uma marca permanente no ecrã. Evita-o a todo o custo. Tudo o que tenha de estar sempre visível deve mover-se, mudar de posição ou desaparecer de forma regular.

Alguns cuidados que fazem diferença numa parede deste formato:

- A imagem é muito larga e baixa. Composições na horizontal, ou que tratam cada monitor como uma coluna, funcionam melhor do que uma imagem centrada.
- Evita pôr texto pequeno ou detalhes importantes em cima das juntas entre monitores.
- A maioria das pessoas vê a parede a andar, a poucos metros de distância. Conteúdos que se percebem em poucos segundos funcionam melhor.
- Não é preciso ter a parede para começar. Os exemplos deste repositório abrem uma pré-visualização à escala, com as juntas marcadas, que corre num portátil.
- Formato de vídeo aceite: `TODO`.

Para propor um trabalho: `TODO` (contacto, formulário ou processo de submissão).

## Exemplos

Os exemplos estão em [`examples/`](examples/) e servem de ponto de partida para estudantes e investigadores. Cada um é pequeno, comentado e corre sem a parede, em modo de pré-visualização.

### Processing

- [`fnp_base`](examples/processing/fnp_base/) — sketch mínimo com a resolução da parede, modo de pré-visualização à escala e as juntas entre monitores marcadas. É o melhor sítio para começar.
- `fnp_screens` — `TODO`: trata cada monitor como uma tela independente, útil para composições em colunas.
- `fnp_camera` — `TODO`: lê uma das câmaras e usa a imagem como entrada para o desenho.
- `fnp_presence` — `TODO`: deteção de movimento simples para reagir a quem passa.
- `fnp_type` — `TODO`: tipografia em movimento ao longo da parede.

`TODO`: exemplos noutras ferramentas (p5.js, TouchDesigner, vídeo).

## Estrutura do repositório

```
feednplay/
├── README.md
├── docs/
│   ├── wall.svg                  diagrama da parede
│   └── tools/
│       └── make_wall_svg.py      gera o diagrama
├── examples/
│   ├── processing/
│   │   ├── fnp_base/
│   │   ├── fnp_screens/
│   │   ├── fnp_camera/
│   │   ├── fnp_presence/
│   │   └── fnp_type/
│   └── p5js/                     TODO
├── templates/                    TODO: modelos de cartaz/anúncio a 9720 × 1920 (Figma, Illustrator, PNG)
└── showcase/                     TODO: imagens e registos de trabalhos já mostrados
```

## História

O FeedNPlay nasceu em 2022, a partir de uma proposta submetida ao programa First Foundation Project no final de 2021 por Tiago Martins, Catarina Maçãs, Evgheni Polisciuc, João M. Cunha, Sérgio Rebelo, João Correia, Pedro Martins, João Bicker e Penousal Machado.

Desde então a parede já recebeu instalações criadas de propósito para ela, serviu de apoio a aulas, dissertações e eventos, e acolheu chamadas abertas a trabalhos da comunidade. Uma segunda proposta ao mesmo programa centrou-se na dimensão interativa: mais sensores e módulos de interação documentados, acompanhados de exemplos de código como os deste repositório.

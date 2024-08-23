# [FLAMBOYANT] VSCode Snippets

Esta extensão contém uma coleção de snippets personalizados para o VSCode, projetados para acelerar o desenvolvimento de projetos utilizando a estrutura [FLAMBOYANT]. Cada snippet permite a criação rápida de componentes, garantindo uma padronização e agilidade no processo de desenvolvimento.

[Documentação](https://learn.zohopublic.com/external/manual/documenta%C3%A7%C3%A3o-flamboyant/article/text-p?p=3843fd39c26dbc5df04c1282f2c7e8b52b84f3bde5c37f006151a3a29c9b799e)

## Índice

- [Uso](#uso)
- [Snippets Disponíveis](#snippets-disponíveis)
  - [Attr](#attr)
  - [Bigtitle](#bigtitle)
  - [Title](#title)
  - [Subtitle](#subtitle)
  - [Text](#text)
  - [Subtext](#subtext)
  - [UL](#ul)
  - [Li](#li)
  - [Image](#image)
  - [ImageComModal](#imagecommodal)
  - [Button](#button)
  - [ButtonModal](#buttonmodal)
  - [Background](#background)
  - [BackgroundCor](#backgroundcor)
  - [BackgroundWidcard](#backgroundwidcard)
  - [BackgroundVideo](#backgroundvideo)
  - [Modal](#modal)
  - [Accordeon](#accordeon)
  - [Card](#card)
  - [ColunaDupla](#colunadupla)
  - [ColunaSimples](#colunasimples)
  - [Guide](#guide)
  - [Holder](#holder)
  - [Iframe](#iframe)
  - [Link](#link)
  - [Line](#line)
  - [List](#list)
  - [Slider](#slider)
  - [Carousel](#carousel)
  - [Audio](#audio)
  - [Video](#video)

## Uso

Digite o prefixo correspondente ao snippet para inserir o componente ou funcionalidade desejada no seu código. Cada snippet vem com placeholders que podem ser navegados usando a tecla `Tab`, permitindo rápida personalização.

## Snippets Disponíveis

### Attr

- **Prefixo:** `!fAttr`
- **Descrição:** Permite a adição de novos atributos a elementos, como funções de clique, sem a necessidade de scripts auxiliares.
- **Exemplo de Uso:**

```javascript
attr:{
  item: 'itemName',
  onClick: 'handleClick()'
},

```

### accordeon

- **Prefixo:** `!fAccordeon`
- **Descrição:** Componente Accordeon que pode receber uma ou duas colunas internamente e abrigar outros componentes.
- **Exemplo de Uso:**

```javascript
{
  type: 'accordeon',
  class: '',
  nextLiberate: false,
  resource: [
    {
      title: {
        content: '',
        class: ''
      },
      body: {
        columns: [
          {
            col: [

            ],
          },
        ]
      }
    },
  ]
}

```

### audio

- **Prefixo:** `!fAudio`
- **Descrição:** Utilizado para incorporar arquivos de áudio no formato MP3.
- **Exemplo de Uso:**

```javascript
{
  type: 'audio',
  resource: {
    class: '',
    classContainer: '',
    src: '*.mp3',
    alt: '',
    attr: {
        loop: false,
        autoplay: false,
        controls: true,
    },
  }
}

```

### Background

**Prefixo:** `!fBackground`  
**Descrição:** Para inserir imagens de fundo.

#### Exemplo de Uso:

```javascript
{
  type: 'background',
  resource: {
    class: 'background-class',
    src: 'background-image.jpg',
    alt: ''
  }
}

```

### BackgroundCor

**Prefixo:** `!fBackgroundCor`  
**Descrição:** Para inserir uma cor de fundo.

#### Exemplo de Uso:

```javascript
{
  type: 'background',
  resource: {
    class: '$1',
    cor: '$2',
    alt: ''
  }
}

```

### BackgroundWidcard

**Prefixo:** `!fBackgroundWidcard`  
**Descrição:** Para inserir uma imagem no fundo do Widcard.

#### Exemplo de Uso:

```javascript
+template-wildcard({
    class: '',
    bg: '',
    columns: [
        {
           col:[

           ]
        },
        {
           col:[

           ]
        }
    ]
}),

```

### BackgroundVideo

**Prefixo:** `!fBackgroundVideo`  
**Descrição:** Para inserir um vídeo como fundo.

#### Exemplo de Uso:

```javascript
+template-wildcard({
    class: '$1',
    video: '$2',
    columns: [
        {
           col:[
              $3
           ]
        },
        {
           col:[
              $4
           ]
        }
    ]
}),

```

### Button

**Prefixo:** `!fButton`  
**Descrição:** Funcionalidade de clique para usar um evento.

#### Exemplo de Uso:

```javascript
{
  type: 'button',
  resource: {
    alt: 'button',
    class: '$1',
    attr: {
       onClick:''
    },
    content: [
      $2
    ]
  },
},

```

### ButtonModal

**Prefixo:** `!fButtonModal`  
**Descrição:** Funcionalidade de clique que pode abrir um Modal (`activeModal`). Exemplo de uso: `#Modal01`.

#### Exemplo de Uso:

```javascript
{
  type: 'button',
  resource: {
    alt: 'button',
    class: '',
    activeModal: '',
    content: [

    ]
  },
},

```

### Card

**Prefixo:** `!fCard`  
**Descrição:** Composição entre um ou mais componentes no sentido vertical.

#### Exemplo de Uso:

```javascript
{
  type: 'card',
  resource: {
    class: '$1',
    content: [
      $2
    ]
  },
},

```

### ColunaDupla

**Prefixo:** `!fColunaDupla`  
**Descrição:** As Colunas Padrões são as mais usadas durante o desenvolvimento de uma peça. A formação pode ser usado em 1 ou 2 colunas padrões na viewport ou com mais colunas caso existam colunas customizadas. O foco principal é a adição de N componentes dentro de cada coluna.

#### Exemplo de Uso:

```javascript
+template -
  wildcard({
    class: "$1",
    columns: [
      {
        type: "01-50",
        col: [
          {
            type: "class",
            resource: "",
          },
          $2,
        ],
      },
      {
        type: "01-50",
        col: [
          {
            type: "class",
            resource: "",
          },
          $3,
        ],
      },
    ],
  });
```

### ColunaSimples

**Prefixo:** `!fColunaSimples`  
**Descrição:** As Colunas Padrões são as mais usadas durante o desenvolvimento de uma peça. A formação pode ser usado em 1 ou 2 colunas padrões na viewport ou com mais colunas caso existam colunas customizadas. O foco principal é a adição de N componentes dentro de cada coluna.

#### Exemplo de Uso:

```javascript
+template -
  wildcard({
    class: "",
    columns: [
      {
        col: [
          {
            type: "class",
            resource: "$1",
          },
          $2,
        ],
      },
    ],
  });
```

### Guide

**Prefixo:** `!fGuide`  
**Descrição:** Elemento com objetivo de deixar uma informação em destaque para guiar alguma ação.

#### Exemplo de Uso:

```javascript
{
  type: 'guide',
  resource: {
    class: '$1',
    content: [
      {
        type: 'image',
        resource: {
          src: '$2',
          class: '',
          alt: '',
        }
      },
      {
        type: 'text',
        resource: {
          content: '$3',
          class: '',
        }
      },
    ]
  }
},
```

### Holder

**Prefixo:** `!fHolder`  
**Descrição:** Elemento auxiliar que fica interno a outros elementos, como Card e Line.

#### Exemplo de Uso:

```javascript
{
  type: 'holder',
  resource: {
    class: '$1',
    content: [
        $2
    ]
  }
},
```

### Image

**Prefixo:** `!fImage`  
**Descrição:** Imagem que precisa estar dentro das limitações das margens.

#### Exemplo de Uso:

```javascript
{
  type: 'image',
  resource: {
    classContainer: '',
    class: '$1',
    src: '$2',
    alt: ''
  }
},
```

### ImageComModal

**Prefixo:** `!fImageComModal`  
**Descrição:** Imagem que precisa estar dentro das limitações das margens, com `data-modal`.

#### Exemplo de Uso:

```javascript
{
  type: 'image',
  resource: {
    classContainer: '',
    class: '$1',
    src: '$2',
    attr: { 'data-modal': '$3' },
    alt: ''
  }
},
```

### Iframe

**Prefixo:** `!fIframe`  
**Descrição:** Utilizado para receber link de iframe.

#### Exemplo de Uso:

```javascript
{
  type: 'iframe',
  resource: {
    classContainer: '',
    class: '$1',
    src: '$2',
    attr: { 'allowfullscreen': 'allowfullscreen' },
    alt: ''
  }
},
```

### Link

**Prefixo:** `!fLink`  
**Descrição:** Tem funcionalidade de clique que por padrão abre um link ou faz o download (pdf, imagem).

#### Exemplo de Uso:

```javascript
{
  type: 'link',
  resource: {
    alt: '',
    classContainer: '',
    class: '$1',
    href: '$2',
    target: '_blank',
    download: 'download',
    content: [
       $3
    ],
    alt: ''
  }
},
```

### Li

**Prefixo:** `!fLi`  
**Descrição:** Elemento filho do UL: `<ul><li></li></ul>`

#### Exemplo de Uso:

```javascript
{
  class: '$1',
  li: '$2',
},
```

### Line

**Prefixo:** `!fLine`  
**Descrição:** Elemento com objetivo de deixar em 2 colunas, uma com fração menor e outra com fração maior.

#### Exemplo de Uso:

```javascript
{
  type: 'line',
  class: '$1',
  dimensions: '$2',
  resource: [
    {
      fraction: 'minor',
      content: [
        $3
      ]
    },
    {
      fraction: 'major',
      content: [
        $4
      ]
    }
  ],
},
```

### List

**Prefixo:** `!fList`  
**Descrição:** Cria uma lista de elementos em sequência.

#### Exemplo de Uso:

```javascript
{
  type: 'list',
  class: '$1',
  resource: [
   $2
  ],
},
```

### Modal

**Prefixo:** `!fModal`  
**Descrição:** Criação do Modal.

#### Exemplo de Uso:

```javascript
+modal("$1", "modal $2") +
  template -
  wildcard({
    bg: "",
    class: "$3",
    columns: [
      {
        col: [
          {
            type: "class",
            resource: "",
          },
          $4,
        ],
      },
    ],
  });
```

### Slider

**Prefixo:** `!fSlider`  
**Descrição:** Slides: Utilizado com a própria estrutura. Em coluna única ou dupla, pode receber outros componentes internamente.

#### Exemplo de Uso:

```javascript
{
  type: 'slides',
  resource: {
    class: '$1',
    nextLiberate: false,
    slides: [
      {
        columns: [
          {
            col: [
              {
                type: 'class',
                resource: ''
              },
               $2
            ]
          },
        ]
      },
      {
        columns: [
          {
            col: [
              {
                type: 'class',
                resource: ''
              },
               $3
            ]
          },
        ]
      },
    ]
  }
},
```

### Carousel

**Prefixo:** `!fCarousel`  
**Descrição:** Carousel: Utilizado em coluna única, pode receber outros componentes internamente. Funciona praticamente da mesma maneira que o Slider, mas se apresenta como um carrossel em loop, sempre destacando o item central. Por isso, para utilizar este componente, precisamos ter, no mínimo, três objetos.

#### Exemplo de Uso:

```javascript
{
   type: 'slides',
   resource: {
    show: 3,
    loop: true,
    class: '$1',
    nextLiberate: false,
    slides: [
      {
        columns: [
          {
            col: [
              {
                type: 'class',
                resource: ''
              },
               $2
            ]
          },
        ]
      },
      {
        columns: [
          {
            col: [
              {
                type: 'class',
                resource: ''
              },
               $3
            ]
          },
        ]
      },
    ]
  }
},
```

### Bigtitle

**Prefixo:** `!fBigtitle`  
**Descrição:** Título destaque do projeto. (H1)

#### Exemplo de Uso:

```javascript
{
  type: 'bigtitle',
  resource: {
    class: '$1',
    content: '$2',
  }
},
```

### Title

**Prefixo:** `!fTitle`  
**Descrição:** Título destaque da seção/tela.(H2)

#### Exemplo de Uso:

```javascript
{
  type: 'title',
  resource: {
    class: '$1',
    content: '$2',
  }
},
```

### Subtitle

**Prefixo:** `!fSubtitle`  
**Descrição:** Título secundário da seção/tela.(H3)

#### Exemplo de Uso:

```javascript
{
  type: 'subtitle',
  resource: {
    class: '$1',
    content: '$2',
  }
},
```

### Text

**Prefixo:** `!fText`  
**Descrição:** Paragrafo do seção/tela.

#### Exemplo de Uso:

```javascript
{
  type: 'text',
  resource: {
    class: '$1',
    content: '$2',
  }
},
```

### Subtext

**Prefixo:** `!fSubtext`  
**Descrição:** Texto de tamanho menor, normalmente utilizado para legendas de imagens..

#### Exemplo de Uso:

```javascript
{
  type: 'subtext',
  resource: {
    class: '$1',
    content: '$2',
  }
},
```

### UL

**Prefixo:** `!fUl`  
**Descrição:** Utilizado para criação de listas `ul > li`.

#### Exemplo de Uso:

```javascript
{
  type: 'ul',
  class: '$1',
  resource: {
    content: [
      {
        class: '$2',
        li: '$3',
      },
    ]
  }
},
```

### Video

**Prefixo:** `!fVideo`  
**Descrição:** Utilizado para receber arquivos de vídeo MP4.

#### Exemplo de Uso:

```javascript
{
  type: 'video',
  resource: {
    class: '$1',
    classContainer: '',
    src: '$2.mp4',
    alt: '',
    attr: {
      loop: false,
      autoplay: false,
      controls: true,
    }
  }
},
```

### Magnet

**Prefixo:** `!fMagnet`  
**Descrição:** Caso precise criar um elemento customizado, como por exemplo um SVG com controles de programação, é possível criar esse elemento no `mixin.custom.pug` com uma classe (identificadora) e acoplar esse mesmo elemento em qualquer local do wildcard e demais templates.

#### Exemplo de Uso:

```javascript
{
  type: 'magnet',
  resource: {
    class: '$1',
    magnetClass: '$2',
  }
},
```

### Flipcard

**Prefixo:** `!fFlipcard`  
**Descrição:** Duplo card, com a lógica de um oculto e que através do evento hover ou clique esse card é apresentado. Internamente, cada um segue a mesma forma de estruturar do card padrão.

#### Exemplo de Uso:

```javascript
{
  type: 'flipcard',
  resource: {
    class: '$1',
    model: 'vertical',
    event: 'click',
    front:[
       {
         type: 'card',
         resource: {
            class: '',
            content: [
               $2
            ]
         }
       },
    ],
    back:[
       {
         type: 'card',
         resource: {
            class: '',
            content: [
               $3
            ]
         }
       },
    ]
  }
},
```

# FUNDAMENTOS

[`introito`](https://github.com/jcarloscody/flutter_fundamentos/blob/master/introito.md) Introdução


- O flutter quebra a barreira linguistica para a construção de aplicativos multi-plataforma.
- é compilado de forma nativa usando uma única fonte de dados.
- reduz o custo e a complexidade da produção de aplicativos em todas as plataformas.
- Não depende da tecnologia de navegador web nem do conjunto de componentes que vem com cada dispositivo.
- o Flutter usa seu próprio mecanismo de renderização de alto desempenho para desenhar os componentes.
- é construído com C, C++, Dart  e Skia(um mecanismo de renderização 2D)
- roda em 60 fps
- ele pode ser interpretado ou compilado
- `hot reload`: funciona injetando arquivos de código-fonte atualizados na Dart VM em execução. isso não apenas adiciona novas classes , mas também adiciona métodos e campos Às classes existentes e altera as funções existentes.
- `hot restart` redefine o estado para o estado inicial do aplicativo

#### O que é Widget?
- tudo no flutter é widget. É uma classe.
- tipos
    - `visíveis`: botão por exemplo
    - `invisíveis`: estrutura o layout por exemplo
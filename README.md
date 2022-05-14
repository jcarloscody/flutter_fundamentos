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


#### StatelessWidget e StatefulWidget
- `estado` é tudo aquilo que temos na tela e queremos que mude ou não.
- `StatelessWidget`: sem estado, componente estático, que não pode haver mudanças. não tem auto alteração.
- `StatefulWidget`: este tem estado, tem a criação de um estado para o controlar. com isto temos uma class que representa o seu estado, e podemos informar para a class stateful que estamos alterando seu estado por meio do método setState, com este método o objeto desta class será marcado como sujo e no próximo ciclo as mudanças serão refletidas. em suma é quando queremos que haja alguma mudança de estado, usamos o stateful
    - `initState()`  é chamado apenas 1x no início quando carregamos a nossa tela antes de construir a nossa class. quando rebuldamos não é chamado novamente.
    

#### Árvore de Componentes
Temos **`3 árvores`**:
- `Árvores de widgets:` o componente propriamente dito, widget. Esta árvore é imutável. 
- `Árvores de elementos:` a estrutura lógia associado ao respectivo componente.
- `Árvore de renderização:` responsável pelo desenho do componente na tela.
> Ou seja, o componente widget é referenciado pelo elemento widget e por sua vez é renderizado na tela pelo renderObject.
> É importante observar que a árvore de **componente é imutável**, mesmo sendo um componente stateless/ful, porém quando alteramos a estrutura lógica, objeto elemento widget e é **marcado como sujo** e isto é informado pelo método setState, a árvore de componente é recriado.


#### Ciclo de vida de Stateful/less
- o ciclo de vida se refere a ordem que alguns métodos são chamados dentro da arquitetura do flutter.
- **`StatelessWidget`**: 
    - construtor
    - build
- **`StatefulWidget`**: esta classe fornece a possibilidade de alterar o estado por meio do método setState e este método irá chamar o build novamente.
    - construtor
    - **`createState`**: vai retornar um objeto da **`class State`**, class para a qual é delegada para controlar o estado.
      - construtor:
      - `initState:` é onde podemos carregar os estados caso tenha necessidade. aqui iremos inicializar todos os dados para a tela funcionar. este método não pode ser assíncrono, pode chamar o .then, mas não pode usar o async/await, 
      - didChangeDependencies: método que é chamado antes de atualizar qq dependências.
      - build: 
  
### Executando funções depois da tela pronta (addPostFrameCallback)
Às vezes estamos numa situação que queremos executar algo antes mesmo de entrarmos em determinada página, por exemplo, ao indentificarmos determinado dado/informação no initState já navegamos para outra página sem antes criar a página que estamos. Para usarmos deste artifício deveremos usar o método [`addPostFrameCallback`](https://github.com/jcarloscody/flutter_fundamentos/blob/master/lib/main.dart) 
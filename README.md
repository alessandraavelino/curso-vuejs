# my-app

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


- Data binding:
    - Possibilidade de mudar em tempo real um dado,
    por meio do que é recebido de um input, por exemplo.

- v-Model:
    - Uma forma de comunicar ao Vue que eu quero salvar
    o dado do input em alguma parte no Vue.

- v-onclick:
    Disparar um evento. 

- Life cycle Hooks
    - São eventos que podem ser ativados em determinadas
    pasrtes da execução do programa.

- Diretivas
    - Pode mudar a exibição de uma parte do layout, baseada em uma condição.
    - Essenciais para aplicação dinâmica.
    - Pode alterar a lógica pelos valores inseridos em data.
    - Tipos de diretivas: 
        - V-if > condições.
        - V-show > única. mostra ou não mostra o componente. 
        - V-bind > Componentização dinâmica;

- Métodos
    - Permitem ser executados baseados em evenetos ou através de alguma lógica
    da aplicação.
    - Eles ficam em um objeto chamado 'methods'.
    - Criaremos funções que serão executadas posteriormente.

- CSS global e scoped
    - global: onde definimos no app, e se aplica a todos os elementos.
    - scoped: onde cada componente pode ter  seu estilo individualmente.

- Renderização de listas
    - As listas serão renderizadas por diretivas.
    - Utilizamos v-for.
    - O dado pode vir de tada, como um array.
    - Cada item pode ser impresso junto do HTML. 

- Eventos
    - São utilizados para complementar ações dos usuários
    com ativações de métodos.
    - @click > é um tipo de evento.
    - Podem ser adicionados direamente a elementos do HTML.
    - O evento recebe um parâmetro que é o método a ser executado.

- Múltiplos eventos
     - Permite executar dois ou mais métodos com um click.

- Reutilização de componentes
    - Ativar métodos e mudar seus dados, quando necessário.
    - Para utilizar o recurso, basta invocar novamente o componente após
    a importação do mesmo.

- Props
    - As props podem ser passadas por valores do data, como também podemos inserir 
    diretamente eles.
    - Precisamos declarar as propriedades recebidas pelos componentes, em um array
    ou objeto chamadod props.

- Emit
    - É posível ouvir um evento de um componente filho em um componente pai.
    - Podemos ativar comportamentos (como métodos) no componente pai.
    - O evento deve ser registrado no componente.
    - E é preciso definir o que será feito com a ativação do evento na chamada do
    componente.

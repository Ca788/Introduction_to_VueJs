## Introdução ao Vue.js

## Sintaxe básica:

body
div id="app"
{{nome}}, {{idade}}, {{email}}
div

script

    const vm = new Vue({
      el: "#app",
      data: {
        nome: "Carlos Lima",
        idade: 24,
        email: "Ducaliima@gmail.com"
      }
    });

    vm.nome = "Duca"
    console.log(vm);

/body

# div id="app": Aqui, um elemento div é criado com o atributo id definido como "app". Isso provavelmente é usado como um ponto de montagem para a aplicação Vue.js. A aplicação Vue será associada a este elemento, permitindo que ela controle e atualize o conteúdo dentro dele.

# {{nome}}, {{idade}}, {{email}}: Estes são placeholders de interpolação do Vue.js, também conhecidos como "interpolations" ou "double curly braces". Eles são usados para exibir valores dinâmicos no HTML. Neste caso, eles exibirão os valores das propriedades nome, idade e email do objeto Vue.

# el: "#app": Isso conecta a instância Vue ao elemento HTML com o id "app", ou seja, a instância Vue irá controlar o conteúdo dentro desse elemento.

# data: Este é um objeto que contém os dados da aplicação. No caso, nome, idade e email são propriedades definidas na seção data.

# vm.nome = "Duca": Aqui, o valor da propriedade nome dentro do objeto Vue é alterado para "Duca". Isso causará uma reatividade no Vue, fazendo com que o conteúdo exibido dentro do elemento com id "app" seja atualizado automaticamente para refletir essa alteração.

# console.log(vm);: Este comando exibe o objeto Vue na console do navegador. Isso pode ser útil para verificar as propriedades e métodos disponíveis na instância Vue.

## Data:

A propiedade data é responsavel por dar a reatividade aos estados definido os seus getters e setters. Ela recebe um objeto ou uma função.

## Proxy:

Toda propiedade dentro de data, é também representada diretamente no objeto Vue(proxy), Se começar com $ ou \_ não é feito proxy para evitar conflito com as propiedades de Vue.

exemplo:

const vm = new Vue({
el: "#app",
data: {
titulo: "Vue.js completo",
$preco: 59
}
});

    vm.$data.titulo = // Vue.js completo
    vm.titulo = // Vue.js completo

    vm.$data.$preco = // 59
    vm.$preco; // undefined

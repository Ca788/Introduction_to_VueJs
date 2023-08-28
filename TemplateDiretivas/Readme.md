## Diretivas:

# v-bind: Liga um atributo a uma expressão, permitindo atualizações dinâmicas.

Exemplo: <img v-bind:src="urlDaImagem">

# v-model: Cria uma ligação bidirecional em um elemento de entrada ou componente.

Exemplo: <input v-model="mensagem">

# v-if: Renderização condicional; o elemento é adicionado ao DOM se a expressão avaliar como verdadeira.

Exemplo: <p v-if="estaVisivel">Isso está visível</p>

# v-for: Renderiza uma lista de itens com base em um array ou objeto.

Exemplo: <li v-for="item in itens">{{ item.nome }}</li>

# v-on: Anexa ouvintes de eventos a elementos do DOM ou componentes.

Exemplo: <button v-on:click="fazerAlgo">Clique em mim</button>

# v-show: Semelhante ao v-if, mas alterna a visibilidade do elemento usando a propriedade CSS display.

Exemplo: <p v-show="estaVisivel">Eu estou visível</p>

# v-pre: Ignora a compilação do Vue para este elemento e todos os seus filhos.

Exemplo: <span v-pre>{{ isto não será compilado }}</span>

# v-cloak: Essa diretiva é usada com CSS para ocultar ligações Mustache não compiladas até que estejam prontas.

Exemplo: <div v-cloak>{{ mensagem }}</div>

# v-once: Renderiza o elemento e seu conteúdo apenas uma vez, sem reatividade.

Exemplo: <p v-once>Isso não mudará</p>

# v-else: Usado com v-if para definir um bloco de else.

Exemplo:
p v-if="estaVisivel">Isso está visível /p
p v-else>Isso não está visível /p

## Templates:

# Interpolação Mustache: Insere o valor avaliado de uma expressão JavaScript no template.

Exemplo: <p>{{ mensagem }}</p>

## Propriedades Computadas: Define propriedades computadas com base em dados reativos.

Exemplo:

computed: {
nomeCompleto() {
return this.primeiroNome + ' ' + this.ultimoNome;
}
}

## Métodos: Define métodos que podem ser chamados a partir do template ou componente.

Exemplo:

methods: {
cumprimentar() {
alert('Olá!');
}
}

## Filtros: Aplica transformações de texto aos dados antes de exibi-los no template.

Exemplo: <p>{{ mensagem | maiusculas }}</p>

## Slots: Permite passar conteúdo do componente pai para o componente filho.

Exemplo:
Componente Pai:

componente-filho
pIsso é passado para o componente filho p

componente-filho
Componente Filho:

div
slot /slot
div

## Definição de Componente: Define componentes personalizados que encapsulam templates, lógica e estilos.

Exemplo:

Vue.component('meu-componente', {
template: 'div{{ mensagem }}div>',
data() {
return {
mensagem: 'Olá do meu componente'
};
}
});

Advanced-JavaScript-I Course
============================

2-Especificando uma Negociação
----------------------------

**1.O que é um modelo?**

Trata-se de uma abstração do mundo real. Por exemplo, um analista de mercado que quer entender como o mercado funciona, criará um modelo em que ele possa dar entradas e executar determinado procedimentos para tentar prever como é o seu funcionamento.


**2.A classe Negociação**

Criando uma classe:

```javascript
class Negociacao {

}
```

Para definir os atributos usa-se a função constructor().

```javascript
constructor() {
    this. ...;
}
```


**6.Objetos Imutáveis**

Congelá-se o objeto dentro do construtor, depois de receber os parâmetros:

```javascript
Object.freeze(this);
```


**7.A instância é imutável mesmo?**

A data, sendo um objeto do tipo Date(), pode ser mudada. Só atributos do objeto criado que serão congelados.


**8.Programação defensiva**

O getTime de uma data retornará um número long com uma representação da data.


**9.Substituindo var por let**

Em JS, quando declaro _var_ não existe escopo de bloco (uma _var_ dentro de um _for_ pode ser acessada fora). Com o _let_ o escopo existe.


3-A ligação entre as ações do usuário e o modelo
----------------------------

função _typeof()_ mostra o tipo de uma variável.

para evitar percorrer o DOM muitas vezes, podemos colocar a obtenção dos dados dentro do construtor do controller.

o objeto _Date_ cria(pelo join) uma string separada por vírgula a partir da data passada para ele.

quando feito assim: _let data = new Date(2017, 10, 30)_ o mês é contado de 0 à 11.

No _ES6_, temos o recurso **spread operator** que significa que o array está desmembrado e cada parâmetro será posicionado na mesma ordem no construtor.

Quando se tem uma só instrução em uma função não precisa colocar o bloco {} e pode ser feito inline e pode-se tb emitir a palavra 'return'.

Exemplo de **Arrow Function**:

```javascript
(item, indice) => item - indice % 2
```

Métodos STATIC -> os métodos são invocados diretamente da classe sem a necessidade de uma instância; métodos que pertencem à definição da classe.

**Template Strings**: maneira mais prática de se concatenar uma string no ES6.

Em vez disso:

```javascript
data.getDate() + '/' + (data.getMonth() + 1)  + '/' + data.getFullYear();
```

fazer desse jeito:

```javascript
`${data.getDate()}/${(data.getMonth()+1)}/${data.getFullYear()}`;
```

**Immediately-invoked function expression (IIFE) ou a função imediata**: Trata-se de um recurso usado na criação de escopo em JavaScript, que nos ajudará a colocar um bloco na expressão, sendo executado imediatamente.

```javascript
(function())()    //esse último conjunto de parenteses é característico do IIFE
```

**função reduce()**: processa o array e no fim, disponibiliza um único resultado. Recebe dois parametros: uma função e o valor inicial de uma das variáveis internas da função que acumulará os resultados do array.

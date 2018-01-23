# Desafio da semana #4

```js
/*
Declare uma variável chamada `isTruthy`, e atribua a ela uma função que recebe
um único parâmetro como argumento. Essa função deve retornar `true` se o
equivalente booleano para o valor passado no argumento for `true`, ou `false`
para o contrário.
*/
var isTruthy = function(a) {
	if (a)
		return true;
	return false;
};

// Invoque a função criada acima, passando todos os tipos de valores `falsy`.
isTruthy("");
false
isTruthy('');
false
isTruthy(0);
false
isTruthy(-0);
false
isTruthy(undefined);
false
isTruthy(null);
false
isTruthy(false);
false

/*
Invoque a função criada acima passando como parâmetro 10 valores `truthy`.
*/
isTruthy("Hello");
true
isTruthy(123);
true
isTruthy(true);
true
isTruthy([]);
true
isTruthy({});
true

/*
Declare uma variável chamada `carro`, atribuindo à ela um objeto com as
seguintes propriedades (os valores devem ser do tipo mostrado abaixo):
- `marca` - String
- `modelo` - String
- `placa` - String
- `ano` - Number
- `cor` - String
- `quantasPortas` - Number
- `assentos` - Number - cinco por padrão
- `quantidadePessoas` - Number - zero por padrão
*/
?

/*
Crie um método chamado `mudarCor` que mude a cor do carro conforme a cor
passado por parâmetro.
*/
var carro = {
	marca: 'Ford',
	modelo: 'Ka',
	placa: 'XXX-1234',
	ano: 1970,
	cor: 'prata',
	quantasPortas: 4,
	assentos: 5,
	quantidadePessoas: 0
}

/*
Crie um método chamado `obterCor`, que retorne a cor do carro.
*/
var obterCor = function(c) {return c.cor;}

/*
Crie um método chamado `obterModelo` que retorne o modelo do carro.
*/
var obterModelo = function(c) {return c.modelo;}

/*
Crie um método chamado `obterMarca` que retorne a marca do carro.
*/
var obterMarca = function(c) {return c.marca;}

/*
Crie um método chamado `obterMarcaModelo`, que retorne:
"Esse carro é um [MARCA] [MODELO]"
Para retornar os valores de marca e modelo, utilize os métodos criados.
*/
var obterMarcaModelo = function(c) {
    var retorno = "Esse carro é um " + c.marca + " " + c.modelo + ".";
    return retorno;
}

/*
Crie um método que irá adicionar pessoas no carro. Esse método terá as
seguintes características:
- Ele deverá receber por parâmetro o número de pessoas entrarão no carro. Esse
número não precisa encher o carro, você poderá acrescentar as pessoas aos
poucos.
- O método deve retornar a frase: "Já temos [X] pessoas no carro!"
- Se o carro já estiver cheio, com todos os assentos já preenchidos, o método
deve retornar a frase: "O carro já está lotado!"
- Se ainda houverem lugares no carro, mas a quantidade de pessoas passadas por
parâmetro for ultrapassar o limite de assentos do carro, então você deve
mostrar quantos assentos ainda podem ser ocupados, com a frase:
"Só cabem mais [QUANTIDADE_DE_PESSOAS_QUE_CABEM] pessoas!"
- Se couber somente mais uma pessoa, mostrar a palavra "pessoa" no retorno
citado acima, no lugar de "pessoas".
*/
var adicionaPessoas = function(n) {
	if (carro.quantidadePessoas === 5) {
		return "O carro já está lotado!";
	}
	else if(carro.quantidadePessoas + n <= 5) {
		carro.quantidadePessoas += n;
		return "Já temos " + carro.quantidadePessoas + " pessoas no carro!"
	} else if (carro.quantidadePessoas + n >= 5 && carro.quantidadePessoas < 5){
		var pessoas = ((5 - carro.quantidadePessoas) === 1) ? "pessoa!" : "pessoas!"
		return "Só cabem mais " + (5 - carro.quantidadePessoas) + " " + pessoas;
	}
}

/*
Agora vamos verificar algumas informações do carro. Para as respostas abaixo,
utilize sempre o formato de invocação do método (ou chamada da propriedade),
adicionando comentários _inline_ ao lado com o valor retornado, se o método
retornar algum valor.

Qual a cor atual do carro?
*/
?

// Mude a cor do carro para vermelho.
?

// E agora, qual a cor do carro?
?

// Mude a cor do carro para verde musgo.
?

// E agora, qual a cor do carro?
?

// Qual a marca e modelo do carro?
?

// Adicione 2 pessoas no carro.
?

// Adicione mais 4 pessoas no carro.
?

// Faça o carro encher.
?

// Tire 4 pessoas do carro.
?

// Adicione 10 pessoas no carro.
?

// Quantas pessoas temos no carro?
?
```

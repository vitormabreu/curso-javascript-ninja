# Desafio da semana #2

Nesse exercício, você está livre para escolher os nomes para suas variáveis e funções! :smile:

```js
// Crie uma função que receba dois argumentos e retorne a soma dos mesmos.
function soma(a, b) {
	return a + b;
}

// Declare uma variável que receba a invocação da função criada acima, passando dois números quaisquer por argumento, e somando `5` ao resultado retornado da função.
var teste = soma(10,7) + 5;

// Qual o valor atualizado dessa variável?
22

// Declare uma nova variável, sem valor.
var nova;

/*
Crie uma função que adicione um valor à variável criada acima, e retorne a string:
    O valor da variável agora é VALOR.
Onde VALOR é o novo valor da variável.
*/
function incrementaNova (incremento) {
	if(nova) {
		nova += incremento;	
    } else {
		nova = 0;
		nova += incremento;
	}
	return "O valor da variável agora é: " + nova + "."
}

// Invoque a função criada acima.
incrementaNova(18);

// Qual o retorno da função? (Use comentários de bloco).
/* "O valor da variável agora é: 18." */

/*
Crie uma função com as seguintes características:
1. A função deve receber 3 argumentos;
2. Se qualquer um dos três argumentos não estiverem preenchidos, a função deve retornar a string:
    Preencha todos os valores corretamente!
3. O retorno da função deve ser a multiplicação dos 3 argumentos, somando `2` ao resultado da multiplicação.
*/
function validaVariaveis (a, b, c) {
	if (!a || !b || !c){
		return "Preencha todos os valores corretamente!";	
	} else{
		var retorno = (a * b * c) + 2;
		return retorno; 
	}
}

// Invoque a função criada acima, passando só dois números como argumento.
validaVariaveis(3,4);

// Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).
"Preencha todos os valores corretamente!"

// Agora invoque novamente a função criada acima, mas passando todos os três argumentos necessários.
validaVariaveis(3,4,5);

// Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).
62

/*
Crie uma função com as seguintes características:
1. A função deve receber 3 argumentos.
2. Se somente um argumento for passado, retorne o valor do argumento.
3. Se dois argumentos forem passados, retorne a soma dos dois argumentos.
4. Se todos os argumentos forem passados, retorne a soma do primeiro com o segundo, e o resultado, dividido pelo terceiro.
5. Se nenhum argumento for passado, retorne o valor booleano `false`.
6. E ainda, se nenhuma das condições acima forem atendidas, retorne `null`.
*/
function somaOuDivisao (a, b, c) {
	if (a && !b && !c){
		return a;
	} else if (b && !a && !c) {
		return b;
	} else if (c && !a && !b) {
		return c;
	} else if (a && b && !c) {
		return a + b;
	} else if(a && !b && c) {
		return a + c
	} else if (!a && b && c) {
		return b + c;
	} else if (a && b && c) {
		var retorno = (a + b) / c;
		return retorno;
	} else if (!a && !b && !c) {
		return false;
	} else {
		return null;
	}
}

// Invoque a função acima utilizando todas as possibilidades (com nenhum argumento, com um, com dois e com três.) Coloque um comentário de linha ao lado da função com o resultado de cada invocação.
somaOuDivisao(3)
3
somaOuDivisao(4, 8 , 5)
2.4
somaOuDivisao(4, null, 3)
7
somaOuDivisao(null, 4, 3)
7
somaOuDivisao(null, 4, 8)
12
somaOuDivisao()
false
somaOuDivisao(undefined, 5, null)
5
somaOuDivisao(undefined, null, null)
false
```

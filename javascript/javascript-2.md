
# Operadores

## Aritméticos: retornam o resultado de uma operação
```
+   somar
-   subtrair
*   multiplicar
/   dividir
%   resto de divisão
```
## Comparadores matemáticos: teste lógico, retorno booleano (true / false):
```
<    menor que
>    maior que
<=   menor ou igual
>=   maior ou igual
```
##### Exemplos 
```
a = 5
b = 4 
1. a < b false
2. a > b true
3. a <= false
4. a >= true
```
 
## Comparadores Lógicos: teste lógico, retorno booleano (true / false)
```
==      igualdade entre sentenças (valor)
!=      diferença entre sentenças (valor)
===     igualdade entre sentenças (valor e tipo)
!==    diferença entre sentenças (valor e tipo)
```

##### Exemplo:
```
a == b = true
a != b = false
```

* Atribuição 
```
a = b
a = 4
```


## Operadores de lógica e junção lógica
```
!       NÃO (NOT)
&&      E (AND)
||      Ou (OR)
```

O sinal de exclamação (!) é o operador NOT (não), utilizado para negar a sentença que vem na sequência. 

#### Exemplos:
```
a != b 		// o valor de a é diferente de b
x !== y	    // o valor e o tipo de x são diferentes de y
!a == b 	// o valor de a não é igual ao valor de b
```

#### As condições lógicas são convertidas em números binários:
true é equivalente a 1
false é equivalente a 0

#### Operador lógico de atribuição

Tem a capacidade de atribuir valor a uma variável a partir de uma condição lógica, economiza IFs

##### Exemplo:
```
var cor = "preto"
var meuCarro = cor == "preto" ? "preto" : "branco";
```

## If
```
if (...) { 
    ...
}
```
## Else 
```
else {

}
```

* Exemplo
```
if (cor == "preto") {
    meuCarro = "preto";
} else {
    meuCarro = "cinza";
}
```

## Else if
```
else if (...) {

}
```

* Exemplo
```
if (cor == "preto") {
    meuCarro = "preto";
} else if (cor == "vermelho"){
    meuCarro = "cinza";
} else if (cor == "amarelo"){
    meuCarro = "branco";
} else {
    meuCarro = "azul";
}
```

## Switch
```
switch (cor) {
    case 'branco' : 
        meuCarro = 'branco';
        break;
    case 'vermelho' : 
        meuCarro = 'vermelho';
        break;
    case 'amarelo' :
        meuCarro = 'amarelo';
        break;
    default : 
        console.log('não temos a cor desejada');
} 
```


## Cálculo média de aluno
```
var nota1 = 10;
var nota2 = 8;
var nota3 = 9;
var nota4 = 7;
var media = (nota1 + nota2 + nota3 + nota4) / 4;
if( media >= 8 ) {
    console.log("Aluno aprovado")
} else {
    console.log("Aluno em recuperação")
}
```

## Laços de Repetição (loops)
for([expressaoInicial]; [condicao]; [incremento]) {
    [execucao]
}

while( [condicao] ){
    [execucao]
}

var contador = 0;
while( contador < 10) {
    contador++
}

```
var hora = 24;
while (hora > 0){
    console.log(hora);
    hora--;
}
```

do {
    [execucao]
} while ([condição])


```
// fazer a revisão do carro aos 10 km
var km;
var revisao = 3;
for(km = 0; km <= revisao; km++ ){
    console.log("apenas " + km + "kms então pode rodar");
}
```

### Cálculo de média de alunos
```
var alunos = [
    [6, 7, 8, 6],
    [8, 5, 6, 8],
    [10, 6, 8, 7],
    [8, 8, 8, 8],
    [6, 6, 6, 6, 6]
]

var nota = 0;
for (var i = 0; i < alunos.length; i++){

    nota = 0
    notasAluno = alunos[i]
    console.log("Aluno: " + parseInt(i+1));
    console.log("Notas: " + notasAluno);

    for( c = 0; c < notasAluno.length; c++ ){
        nota += notasAluno[c];
    }

    media = nota / 4;

    if(media >= 7) {
        resultado = "aprovado";
    } else {
        resultado = "reprovado";
    }

    console.log("Media: " + media + " - " + resultado);

}
```

## Funções

- Evitar a repetição de código
- Realizar chamadas dinâmicas de algoritmos

```
function calcularMedia( notas ) {

    let soma = 0;
    for( c = 0; c < notas.length; c++) {
       soma += notas[c];
    }

    media = soma / notas.length;

    return media;

}

let media; // escopo global

function aprovacao( notas ) {

	let media = calcularMedia( notas ); // escopo da função

	let condicao = media >= 8 ? "aprovado" : "reprovado";
  
    return 'Média: ' + media + ' - Resultado: ' + condicao;

}


// console.log()

//console.log( "Média: " + calcularMedia([8, 8, 7]))
console.log( aprovacao([8, 8, 7]) );


//console.log( "Média: " + calcularMedia([8, 8, 10, 6]))
console.log( aprovacao([8, 8, 10, 6]) );


//console.log( "Média: " + calcularMedia([9, 6]))
console.log( aprovacao([9, 6]) );
```

### Exercício
```
Resultados:
10 + 15 = 25 (Number)
"10" + 2 = "102" (String)
"10" * 2 = 20 (Number)
"10" / 3 = 3.3333333333333335 (Float)
"10" % 3 = 1 (Number)
10 + true = 11 (Number)
10 == "10" = true (Boolean)
10 === "10" = false (Boolean)
10 < 11 = true (Boolean)
10 > 12 = false (Boolean)
10 <= 10.1 = true (Boolean)
10 > 9.99 = true (Boolean)
10 != "dez" = true (Boolean)
10 + true = 11  (Number)
"dez" + true = (desculpe, esse não consegui compreender)
10 + false = 10 (Number)
10 * false = 0 (Number)
true + true = 2  (Number)
10++  (desculpe, esse não consegui compreender)
10--  (desculpe, esse não consegui compreender)
1 & 1 = 1 (Number)
1 & 0 = 0 (Number)
0 & 0 = 0 (Number)
0 / 1 = 0 (Number)
5 + 5 == 10 = true (Boolean)
"5" + "5" == 10 = false (Boolean)
"5" * 2 > 9 = true (Boolean)
(10 + 10) * 2 = 40 (Number)
10 + 10 * 2 = 30 (Number)

```
### Exercício 2

```
A) var branco = "preto" = false
b) var preto = "cinza" = false
C) var cinza = "branco" = false
D) var carro = "preto" = true
E) var prestacao = 750; = 750
F) branco == "branco" = false
G) branco == cinza (desculpe, esse não consegui compreender)
H) carro === branco = false
I) var cavalo = carro == “preto” ? “cinza” : “marron”; = "cinza"
J) Quantas prestações são necessárias para pagar o valordo carro com uma entrada de 3.000? Demonstre a operação
var valorCarro = 3000; // Valor total do carro
var entrada = 3000; // Valor da entrada
var prestacao = 750; // Valor de cada prestação
var numeroPrestacoes = (valorCarro - entrada) / prestacao;
numeroPrestacoes = (3000 - 3000) / 750;
numeroPrestacoes = 0 / 750;
numeroPrestacoes = 0;
K) Somando as variáveis de cores é formada uma stringde quantos caracteres?
somaCores = "preto" + "cinza" + "branco" + "preto";
var quantidadeCaracteres = somaCores.length;
20 caracteres.
```

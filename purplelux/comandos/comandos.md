# Lista de comandos do PurpleLux

## /write

escreve na tela
Equivalente ao print, echo etc...

se usa as abreviações dos tipos de dados para especificar o tipo do dado a ser escrito (não necessário). exemplo:

```
>>> /write str: "Olá, Mundo!";
Olá, Mundo!
```

Para usar o valor que está dentro de uma variável, se usa apenas o nome dela, sem o "v."

```
>>> v.num = 5;
>>> /write num;
5
```

___

## /input

Pede uma entrada do usuário. O parâmetro "text:" mostra o texto antes da entrada.

``` 
>>> /input text: "Digite um número: ";
Digite um número: 27 <- entrada do usuário
```

___

Para atribuir o valor da entrada do usuário à uma variável, é só declarar a variável logo atrás do comando:

```
>>> v.num = /input text: "Digite um número: ";
Digite um número: 30
>>> /write num;
30
```

___

## /repeat

o /repeat serve para repetir um código com um limite determinado.

esse limite é definido pelo parâmetro times:

```
/repeat times: 5 {
    /write "Olá";
}
```

___

## /search

o search significa "pesquisar". e é exatamente isso que ele faz.

ele pesquisa por coisas dentro de algo.

entre vários usos, está em procurar por uma letra ou palavra, por exemplo, dentro de uma string:

```
v.estado = "Rio de Janeiro";
/search for:'o', in:estado
```

nesse exemplo acima vemos dois parâmetros: o for e o in.

o parâmetro for é o que vamos pesquisar;

E o in é onde vamos pesquisar.

Nesse caso, vamos pesquisar a letra "r" dentro da string da variável estado.

também podemos usar o parâmetro position caso tenha mais de uma letra dentro de uma string:

```
/search for:'o', in:estado, position:1;
```

nesse caso ele vai pegar a segunda letra "o" de "Rio de Janeiro".

IMPORTANTE! A capitalização das letras fazem muita diferença.

se formos procurar por "r" em "Rio de Janeiro", vamos encontrar o último "r" na palavra "Janeiro".

Já se procurarmos por "R", vamos encontrar o primeiro "R" na palavra "Rio".

___

Outra forma de usar o search é fazendo o oposto de procurar a posição com a letra.

Podemos procurar a letra pela posição, sem se preocupar com qual letra queremos pegar. para isso, não usamos o for, apenas o in e o position:

```
/search position:8, in:estado;
```

nesse caso ele vai retornar o valo "a" que é o 9° caractere (Já que os espaços também contam).

### Valores do position

Alguns outros valores além de números que podemos dar ao parâmetro position são:

first: procura pelo primeiro caractere ou conjunto de caracteres (mesma coisa que a posição 0)

last: procura pelo último caractere ou conjunto de caracteres

___

Vamos atribuir a posição de um caractere ou o caractere em si à uma variável:

```
v.letra = /search for:"o", in:estado, position:1;
/write letra
```

resultado:
```
"o"
```

também podemos procurar por apenas uma letra e ver na tela qual posição ela está:

```
v.letra = /search for:"d", in:estado;
/write letra-position
```

resultado:

```
4
```

o -position é um modificador que procurará pela posição do caractere retornado para a variável letra. ou seja, 4.


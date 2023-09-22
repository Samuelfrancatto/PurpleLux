# Lista de comandos do Purplescript

## /write

escreve na tela
Equivalente ao print, echo etc...

se usa as abreviações dos tipos de dados para especificar o tipo do dado a ser escrito (não necessário). exemplo:

```
>>> /write str: "Olá, Mundo!";
Olá, Mundo!
```

para escrever o valor que está dentro de uma variável, apenas adiciona na frente do /write o nome da variável junto vom o "v."

```
>>> v.num = 5;
>>> /write v.num;
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
>>> /write v.num
30
```
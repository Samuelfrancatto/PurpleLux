# Lista de comandos do Purplescript

## /write

escreve na tela
Equivalente ao print, echo etc...

se usa as abreviações dos tipos de dados para escrever. exemplo:

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
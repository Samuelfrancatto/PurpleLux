# Lista de comandos do Purplescript

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
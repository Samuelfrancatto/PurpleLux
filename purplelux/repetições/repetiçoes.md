# Repetições em Purplescript

## /while

o while, assim como em outras linguagens, executa um código enquanto uma condição for stisfeita.

```
v.ex = true
/while ex == true {
    bloco de código a ser executado
}
```

Um recurso interessante é usar o "++" para adicionar 1 ao valor de uma variável:

```
v.counter = 0
/while counter < 5{
    /write counter
    counter++
}
```

resultado:
```
0
1
2
3
4
```

um outro tipo de repetição, o /repeat pode ser visto na página COMANDOS.
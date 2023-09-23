# Condições em Purplescript

## /if

significa "se".

funciona assim:

```
/if condição {
    bloco de código
}
```

exemplo:

```
>>> v.num = 24;
>>> /if num == 24 {
        /write "true";
};
```

___

## /else

significa "se não". é usado depois do /if

exemplo:

```
>>> v.num = 8;
>>> /if num == 8{
        /write "true";
} /else{
        /write "false";
}
```

___

/else-if

significa "se não, se". equivalente ao elif do Python.

exemplo:

```
>>> v.num = 10;
>>> /if num > 10{
        /write "Maior";
} /else-if num < 10{
        /write "Menor";
} /else{
        /write "Mesmo valor";
}
```
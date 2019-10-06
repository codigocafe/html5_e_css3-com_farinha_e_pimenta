# Validação de formulários

## Pattern
O atributo pattern nos permite definir expressões regulares de validação, sem Javascript.
```
    <input type="text" name="cep" required pattern="\d{5}-?\d{3}">
```

## Novalidate e Formnovalidate
Podem haver situações em que você precisa que um formulário não seja validado. Neste casos, basta incluir o atributo `novalidade` no elemento `form`.

```
    <form method="post" action="" novalidate>
        ...
    </form>
```

Outra situação comum é querer que o formulário não seja validado dependendo da ação de `submit`. Nesse caso, você pode usar no botão de `submit` o atributo `formnovalidate`.
```
    <form method="post" action="">
        ...
        <input type="submit" value="Submit" formnovalidate>
    </form>
```
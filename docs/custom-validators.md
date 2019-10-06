# Custom Validators

## oninput
O evento `oninput` é diferente do `onchange`, o `oninput` é disparado quando o campo possui alguma alteração em seu valor durante a edição já o `onchange` faz o disparo no final da edição.  
O `oninput` também é diferente dos eventos `onkeyup` e `onkeypress` onde ele também identifica alterações feitas com o mouse.

```
    <input type="text" name="cpf" oninput="validarCPF()">
```
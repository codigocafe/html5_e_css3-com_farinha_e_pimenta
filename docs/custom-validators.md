# Custom Validators

## oninput
O evento `oninput` é diferente do `onchange`, o `oninput` é disparado quando o campo possui alguma alteração em seu valor durante a edição já o `onchange` faz o disparo no final da edição.  
O `oninput` também é diferente dos eventos `onkeyup` e `onkeypress` onde ele também identifica alterações feitas com o mouse.

```
    <input type="text" name="cpf" oninput="vCPF( this )">
```

Você também pode utilizar o método `setCustomValidity` onde ele recebe um `string` e se essa `string` estiver vázia ele retorna como válido, caso ao contrário, retorna inválido.

```
    <!-- arquivo que possui a função validaCPF -->
    <script type="text/javascript" src="validacpf.js"></script>

    <sript type="text/javascript">
        function vCPF(i){
            i.setCustomValidity( validaCPF(i.value) ? '' : 'CPF inválido' );
        }
    </script>
```
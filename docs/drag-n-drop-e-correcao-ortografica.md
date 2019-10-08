# Drag-n-Drop e correção ortográfica

## Drag and Drop
A API de Drag and Drop é relativamente simples. Basicamente, inserir o atributo `draggable="true"` num elemento o torna arrastável. E há uma série de eventos que você pode tratar.

- **dragstart**  
O objeto começou a ser arrastado. O evento que a função recebe em um atributo target, que contém o objeto sendo arrastado.
- **drag**  
O objeto está sendo arrastado.
- **dragend**  
A ação de arrastar terminou

O objeto sobre o qual outro é arrastado sofre os seguintes eventos:

- **dragenter**  
O objeto sendo arrastado entrou no objeto target.
- **dragleave**  
O objeto arrastado deixou o objeto target.
- **dragover**  
O objeto sendo arrastado se move sobre o objeto target.
- **drop**  
O objeto sendo arrastado foi solto sobre o objeto target.

**Detalhes importantes**  

A ação padrão do evento `dragover` é cancelar a ação de *dragging* atual. Assim, nos objetos que devem receber `drop`, é preciso setar uma ação de `dragover` com, no mínimo, `return false`.  

Seleções de texto são automaticamente arrastáveis, não precisam do atributo `draggable`. E se você quiser criar uma área para onde seleções de texto possam ser arrastadas, basta tratar esse mesmo eventos.

Por fim, todas funções de tratamento de evento de `drag` recebem um objeto de evento que contém uma propriedade `dataTransfer`, um *dataset* comum a todos os eventos durante essa operação de `drag`.

## Revisão Ortográfica e Gramatical

Os desenvolvedores podem controlar o comportamento da ferramente de Revisão ortográfia através do atributo `spellcheck`. Para ativar essa ferramenta você adicionar o atributo `spellcheck="true"` e para desativar utilize `spellcheck="false"`.

```
    <textarea name="mensagem" spellcheck="true">
        ...
    </textarea>
```
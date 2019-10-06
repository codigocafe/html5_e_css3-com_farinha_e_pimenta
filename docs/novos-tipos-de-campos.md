# Novos tipos de campos

- Telefone
Telefone. Não há máscara de formatação ou validação, propositalmente, visto não haver no mundo um padrão bem definido para números de telefones.  
    <input type="tel" name="telefone">

- Search
Um campo de busca. A aparência e comportamento do campo pode mudar ligeiramente dependendo do agente de usuário, para parecer com os demais campos de busca do sistema.  
    
    <input type="search" name="busca">
    

- Datas e Horas  
    
    <input type="datetime" name="data" >
    <input type="date" name="data" >
    <input type="month" name="mes" >
    <input type="week" name="semana" >
    <input type="time" name="hora" >
    <input type="datetime-local" name="data-hora" >
    

- Number
Por padrão o campo utiliza números inteiros, para alterar para decimal você precisa alterar o atributo `step` com um valor fracionado, exemplo `0.2`.  
    
    <input type="number" step="1" min="0" max="100" name="numero">
    

- Range  
    
    <input type="range" step="1" min="0" max="100" name="range">
    

- Color  
    
    <input type="color" name="cor">
    
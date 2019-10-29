# Canvas VS SVG

Uma dúvida muito comum é quando usar `Canvas`, quando usar `SVG`. Para saber escolher, é preciso entender as diferenças entre um e outro. SVG é vetorial, e baseado em XML, logo, acessível via DOM. Canvas é desenhado pixel a pixel, via Javascript.  

Assim, as vantagens do SVG são:

- O conteúdo é acessível a leitores de tela;
- O gráfico é escalável, não perde resolução ou serrilha ao redimensionar;
- O conteúdo é acessível via DOM.

E as vantagens do Canvas:

- A performance é muito superior ao SVG na maioria dos casos;
- É facil desenhar via Javascript. Em SVG, é preciso fazer seu script escrever XML para você. Com Canvas você só manda desenhar, e pronto.
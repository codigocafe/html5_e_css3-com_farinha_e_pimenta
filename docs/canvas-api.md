# Canvas API

## O elemento Canvas

A Canvas API permite a você desenhar na tela do navegador via Javascript. O único elemento HTML existente para isso é o elemento `canvas`, o resto todo é feito via Javascrit.

```
    <canvas id="x" width="300" height="300"></canvas>
```

Isso vai exibir um retângulo vazio. Para desenhar nele, primeiro obtemos o contexto de desenho, com Javascript.

```
    context = document.getElementById( 'x' ).getContext( '2d' );
```

Agpra que temos um contexto, podemos desenha nele. Vamos começar com um simples retângulo.

```
    context.fillRect( 10, 10, 50, 150 );
```

Simples, não? Que tal tentarmos algo um pouco mais complexo?

```
    <canvas id="x" width="300" height="300"></canvas>
    <button onclick="desenhar()">desenhar</button>

    <script type="text/javascript">
        function desenhar(){
            //obtemos o contexto
            context = document.getElementById( 'x' ).getContext( '2d' );

            //iniciamos um novo desenho
            context.beginPath();

            //movemos a caneta para o inicio do desenha
            context.moveTo( 150, 50 );

            //desenhamos as linhas
            context.lineTo( 220, 250 );
            context.lineTo( 50, 125 );
            context.lineTo( 250, 125 );
            context.lineTo( 80, 250 );
            context.lineTo( 150, 50 );

            //o desenho não é de verdade enquanto você não mandar o contexto pintá-lo

            //vamos pintar o interior de amarelo
            context.fillStyle = '#FF0';
            context.fill();

            //vamos pintar as linas de vermelho
            context.strokeStyle = '#F00';
            context.stroke();
        }
    </script>
```
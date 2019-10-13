# Elementos audio e videos, e codecs

## Áudio
```
    <audio src="mus.oga" controls="true" autoplay="true">
```
O valor de `controls` define se um controle de áudio, com botões de *play*, *pause*, volume, barra de progresso, contador de tempo, etc. será exibido na tela. Se for setado como "*false*", será preciso controlar o player via javascript, com o métodos como `play()` e `pause()`. O valor de *autoplay* define se o áudio vai começar a tocar assim que a página carregar.

### Origens alteranativas de áudios
```
    <audio controls="true" autoplay="true">
        <source src="mus.oga">
        <source src="mus.mp3">
        <source src="mus.wma">
    </audio>
```

## Vídeo
```
    <video src="u.ogv" width="400" height="300">
```

```
    <video controls="true" autoplay="true" width="400" height="300">
        <source src="u.ogv">
        <source src="u.mp4">
        <source src="u.wmv">
        <p>Faça o <a href="u.mp4">download do vídeo</a>.</p>
    </video>
```

## Codecs
É muito importante que você inclua, nos seus elementos `source` de áudio e vídeo, informação a respeito do container e *codecs* utilizados. Isso vai evitar que o navegador tenha que baixar, pelo menos parcialmente, o arquivo de mídia para, depois, descobrir que não consegue tocá-lo. É importante lembrar que a extensão do arquivo não é informação relevante para isso, pelo contrário, não significa nada. Uma URL pode não ter extensão de arquivo e pode levar a um redirecionamento.  

Para indicar ao navegador o container e *codecs* de determinado arquivo, usa-se o atributo *type*, no formato:
```
    type="mine-type do container. codecs='code de video, codec de audio'"
```

Por exmeplo, um vídeo em Ogg, usando os codecs Theora e Vorbis, terá seu source assim:
```
    <source src="video.ogv" type="video/ogg; codecs='theora,vorbis'">
```

Com o *MPEG-4* a coisa é um pouco mais complicada, por que é preciso indicar ao navegador também o *profile* do *codec* de vídeo utilizado. Veja um exemplo:
```
    <source src="video.mp4" type="video/mp4; codecs='mp4v.20.240, mp4a.40.2'">
```

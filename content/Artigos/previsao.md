Title: Criando overlay com a previsão do tempo 
Date: 2021-05-10 10:20
Category: Artigos
Tags: html, tutorial


Após várias pessoas perguntarem se eu estava com frio durante as [lives na Twitch](https://www.twitch.tv/bug_elseif), surgiu a ideia de colocar um overlay com a previsão do tempo, mostrando a temperatura atual da minha localização.

Foi possível fazer isso de uma maneira simples, usando uma página HTML e uma API.
#### Vamos aos passos:
<enter>

_Primeiramente, criamos um arquivo com a estrutura básica de HTML:_

```html
<!DOCTYPE html>
    <html lang="pt-br">
        <head>
            <meta charset="UTF-8">
            <title>Titulo</title>
        </head>
        <body>
        </body>
    </html>
```
<enter>

_Dentro do corpo do HTML, criamos uma tag `<img>` da seguinte forma:_

```html
    <img src="http://wttr.in/~Lages+Brazil_tqp0.png">
```
<enter>

Desta maneira acessamos a API que nos retorna uma imagem `.png`, através do link vamos passar alguns parâmetros, são eles:
* Localização - informa o nome da cidade e país;
* t - aplica transparência na imagem;
* q- retira o texto “previsão do tempo” deixando só o nome da cidade e país como título;
* p - adiciona uma borda ao redor da imagem;
* 0 - deixa visível somente o clima no momento atual.

Além destes, existem [outros parâmetros](http://wttr.in/:help) que modificam a imagem.

<enter>
_Por fim adicionamos um `<meta>` tag que atualizará a página em determinado tempo (em segundos):_

```html
    <meta http-equiv="refresh" content="300" />
```
<enter>
_A estrutura final do código fica assim:_
```html
<!DOCTYPE html>
    <html lang="pt-br">
        <head>
            <meta charset="UTF-8">
            <meta http-equiv="refresh" content="300" />
            <title>Previsão do tempo</title>
        </head>
        <body>
            <img src="http://wttr.in/~Lages+Brazil_tqp0.png" >
        </body>
    </html>
```

<enter>

_Gerando este resultado:_

![Retângulo contendo informações sobre o clima](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/c5fa1u8jg5zp0bhw1pn9.png)

<enter>
Com a página pronta, basta adicionar uma fonte de navegador no OBS com o caminho no qual o arquivo HTML foi salvo.

<enter>
Mais informações sobre a API [neste github](https://github.com/chubin/wttr.in).
<enter>

Enjoy!


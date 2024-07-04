# Entendendo o Código Fonte de Sites

## Introdução

A maioria dos sites usa três principais tecnologias:
- **HTML**: Estrutura o conteúdo do site.
- **CSS**: Define o design e o layout.
- **JavaScript**: Adiciona funcionalidades interativas.

## Visualizando o Código Fonte

Embora o código-fonte do site esteja disponível no lado do cliente (no navegador), geralmente não o vemos. Para entender como uma página funciona, podemos olhar o código-fonte.

### HTML

HTML define a estrutura e o conteúdo do site. Para ver o código HTML de uma página, você pode:
1. Abrir o site no navegador.
2. Pressionar `CTRL + U` no teclado.

Isso abrirá uma nova aba mostrando o código HTML da página.

Exemplo:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Minha Página</title>
</head>
<body>
    <h1>Título</h1>
    <p>Parágrafo de texto.</p>
</body>
</html>
````

### CSS define o estilo da página. Ele pode ser:

- Interno: Dentro do próprio arquivo HTML, entre as tags `<style>`.
- Externo: Em um arquivo separado, referenciado no HTML.
- Exemplo de CSS interno:

```
<style>
    body {
        background-color: lightblue;
    }
    h1 {
        color: navy;
    }
</style>
```
## Exemplo de CSS externo:
````
<head>
    <link rel="stylesheet" href="style.css">
</head>
````

## JavaScript
JavaScript adiciona funcionalidades interativas ao site. Ele também pode ser:

- Interno: Dentro do próprio arquivo HTML, entre as tags `<script>`.
- Externo: Em um arquivo separado, referenciado no HTML.

### Exemplo de JavaScript interno:

````
<script>
    alert("Olá, mundo!");
</script>
````

### Exemplo de JavaScript externo:

```
<script src="script.js"></script>
```

### Exemplo Prático
Vamos supor que você visite um site que não parece ter muita funcionalidade visível e quer entender o que está acontecendo no código.

Abrir o site: Suponha que o URL é http://SERVER_IP:PORT.
Ver o código-fonte HTML: Pressione CTRL + U.
Você verá algo como:

```
<!DOCTYPE html>
<html>
<head>
    <title>Gerador de Serial Secreto</title>
    <style>
        h1 {
            font-size: 144px;
        }
        p {
            font-size: 64px;
        }
    </style>
    <script src="secret.js"></script>
</head>
<body>
    <h1>Gerador de Serial Secreto</h1>
    <p>Não há campos de entrada visíveis.</p>
</body>
</html>
```
## JavaScript Ofuscado
Às vezes, o JavaScript é "ofuscado", o que significa que o código é deliberadamente tornado difícil de ler. Isso pode parecer algo assim:

## javascript
```
eval(function (p, a, c, k, e, d) { e = function (c) { ... });
```

A ofuscação é usada para dificultar a compreensão e a cópia do código por outras pessoas. É como um código secreto para os desenvolvedores.


# Deobfuscação
Agora que entendemos como funciona a obfuscação de código, vamos começar a aprender sobre deobfuscação. Assim como existem ferramentas para obfuscar automaticamente o código, também existem ferramentas para formatar e deobfuscar o código automaticamente.

## Formatação
Vemos que o código atual está todo escrito em uma única linha. Isso é conhecido como código JavaScript minificado. Para formatar corretamente o código, precisamos "beautify" ou "formatar" o nosso código. O método mais básico para fazer isso é através das ferramentas de desenvolvedor do navegador.

Por exemplo, se estivéssemos usando o Firefox, poderíamos abrir o depurador do navegador com CTRL+SHIFT+Z, e então clicar em nosso script secret.js. Isso mostrará o script em sua formatação original, mas podemos clicar no botão '{ }' na parte inferior, que irá formatar o script adequadamente em JavaScript:

Além disso, podemos utilizar muitas ferramentas online ou plugins de editores de código, como Prettier ou Beautifier. Vamos copiar o script secret.js:

javascript
```
eval(function (p, a, c, k, e, d) { e = function (c) { return c.toString(36) }; if (!''.replace(/^/, String)) { while (c--) { d[c.toString(a)] = k[c] || c.toString(a) } k = [function (e) { return d[e] }]; e = function () { return '\\w+' }; c = 1 }; while (c--) { if (k[c]) { p = p.replace(new RegExp('\\b' + e(c) + '\\b', 'g'), k[c]) } } return p }('g 4(){0 5="6{7!}";0 1=8 a();0 2="/9.c";1.d("e",2,f);1.b(3)}', 17, 17, 'var|xhr|url|null|generateSerial|flag|HTB|flag|new|serial|XMLHttpRequest|send|php|open|POST|true|function'.split('|'), 0, {}))
```
Podemos ver que ambos os sites fazem um bom trabalho em formatar o código:
```
https://prettier.io/playground/
https://beautifier.io/
```

No entanto, o código ainda não é muito fácil de ler porque ele não apenas foi minificado, mas também obfuscado. Portanto, apenas formatar ou "beautify" o código não será suficiente. Para isso, precisaremos de ferramentas para deobfuscar o código.

## Deobfuscação
Podemos encontrar muitas boas ferramentas online para deobfuscar código JavaScript e transformá-lo em algo que podemos entender. Uma boa ferramenta é o UnPacker. Vamos tentar copiar nosso código obfuscado acima e executá-lo no UnPacker clicando no botão UnPack.

Dica: Certifique-se de não deixar nenhuma linha em branco antes do script, pois isso pode afetar o processo de deobfuscação e fornecer resultados imprecisos.

```
https://matthewfl.com/unPacker.html 
```
Podemos ver que essa ferramenta faz um trabalho muito melhor ao deobfuscar o código JavaScript e nos dá um resultado que podemos entender:

javascript
```
function generateSerial() {
  ...SNIP...
  var xhr = new XMLHttpRequest;
  var url = "/serial.php";
  xhr.open("POST", url, true);
  xhr.send(null);
};
```
Como mencionado anteriormente, o método de obfuscação usado acima é conhecido como "packing". Outra maneira de desempacotar esse tipo de código é encontrar o valor de retorno no final e usar console.log para imprimi-lo em vez de executá-lo.

## Engenharia Reversa
Embora essas ferramentas estejam fazendo um bom trabalho até agora em limpar o código para algo que podemos entender, quando o código se torna mais obfuscado e codificado, se torna muito mais difícil para ferramentas automatizadas limpá-lo. Isso é especialmente verdadeiro se o código foi obfuscado usando uma ferramenta de obfuscação personalizada.

Nesses casos, precisaríamos fazer engenharia reversa manualmente no código para entender como ele foi obfuscado e sua funcionalidade. Se você estiver interessado em saber mais sobre Deobfuscação Avançada de JavaScript e Engenharia Reversa, você pode conferir o módulo Secure Coding 101, que deve cobrir este tópico de forma abrangen
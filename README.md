# <strong> Exemplo de Utiliza��o de Express�es Regulares com Dart </strong>

Reposit�rio de Exemplos Criados com Base no Curso de Regex do <strong> Cod3R </strong> na plataforma UDEMY
 - [UDEMY - Fundamentos de Express�es Regulares (Regex)](https://www.udemy.com/course/curso-regex/)

Literatura indicada
 - [Express�es Regulares Cookbook: Solu��es detalhadas em oito linguagens de programa��o](https://www.amazon.com/Express%C3%B5es-Regulares-Cookbook-detalhadas-programa%C3%A7%C3%A3o-ebook/dp/B07YBM728N)
 - [Express�es Regulares - 5a edi��o: Uma Abordagem Divertida](https://www.amazon.com.br/Express%C3%B5es-Regulares-Uma-Abordagem-Divertida/dp/8575224743/ref=asc_df_8575224743/?tag=googleshopp00-20&linkCode=df0&hvadid=379748659420&hvpos=&hvnetw=g&hvrand=9930736693242346207&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9101046&hvtargid=pla-423044219264&psc=1)
 - [Beginning regular expressions](https://www.amazon.com.br/Beginning-Regular-Expressions-Andrew-Watt/dp/0764574892)

# <strong> O que s�o Express�es Regulares ? </strong>

Uma express�o regular (ou "regex") � um padr�o de pesquisa usado para corresponder a um ou mais caracteres num corda. Ele pode corresponder caracteres espec�ficos, curingas e intervalos de caracteres. Express�es regulares foram originalmente usadas por Unix utilit�rios, como vi e grep. No entanto, agora eles s�o suportados por muitas edi��es de c�digo. aplica��es e processadores de texto em v�rias plataformas. Express�es regulares tamb�m podem ser usadas na maioria dos linguagens de programa��o.

Uma express�o regular pode ser t�o simples quanto uma string b�sica, como "app". O regex"app"corresponderia a seq��ncias contendo as palavras" apps "," applications "e" inaplicable ". Uma express�o regular tamb�m pode conter caracteres �ncora (" ^ "e" $ "), usados ??para especificar o in�cio e o final de uma linha, respectivamente. Portanto, o regex "^ aplicativos"corresponderia � sequ�ncia", os aplicativos s�o �timos ", mas n�o corresponderia � sequ�ncia" Eu gosto de aplicativos ".

Express�es regulares podem incluir tra�os, que s�o usados ??para corresponder a um intervalo de caracteres, como todas as letras min�sculas. Por exemplo, a regex "[az]"corresponderia a" aplicativos ", mas n�o corresponderia �s seq��ncias de caracteres" Apps "ou" 123 ". A express�o regular"[A-Za-z]"corresponderia a" Apps "e"[0-9]"corresponderia a" 123 ". Um per�odo, que � o padr�o curinga caractere em express�es regulares, pode ser usado para corresponder a qualquer caractere (exceto um caractere de fim de linha). Um per�odo seguido por um asterisco (. *) Corresponde a zero ou mais inst�ncias, enquanto um per�odo seguido por um sinal de mais (. +) Corresponde a uma ou mais inst�ncias.

Ent�o, o que acontece se voc� precisar corresponder a uma sequ�ncia que contenha um tra�o, asterisco, mais ou um caractere �ncora? Esses caracteres podem ser inclu�dos em um padr�o de express�o regular "escapando" deles com uma barra invertida ("\"). Por exemplo, para pesquisar "$ 0.99", a regex seria "\ $ 0 \ .99". As barras invertidas tamb�m s�o usadas para procurar caracteres n�o imprim�veis. Por exemplo," \ r "corresponde a um retorno de carro," \ n "corresponde a uma nova linha e" \ t "corresponde a um caractere de tabula��o.

Embora n�o seja necess�rio muito esfor�o para criar uma express�o regular b�sica, escrever uma regex avan�ada n�o � uma tarefa f�cil. Mesmo os melhores programadores raramente obt�m express�es regulares complexas logo na primeira vez. Quando usadas corretamente, no entanto, express�es regulares s�o uma ferramenta poderosa para pesquisar, localizar e substituir texto espec�fico.

A express�o regular relaciona todas as ocorr�ncias (matches) de um padr�o (pattern) em um trecho de texto (subject).

| termo	    | significado
| - | -
| matches	| Casar, encontrar, combinar, ocorr�ncias, conferir, encaixar e igualar.
| pattern	| Padr�o, a express�o regular propriamente dita. String de padr�o de procura.
| subject	| Texto que ser� vasculhado por nossa expres�o regular.

# <strong> Como Executar RegExp no Dart </strong>

```dart

void main() {

  /*
   * Express�o Regular
   *  - inicia-se com o "r" depois a String da Express�o "[a-c]"
   * Exemplo:
   *  - r"[a-c]"
  */

  /* String do Texto a Ser Analisado*/

  String texto = "ABC [abc] a-c 1234";

  /*
   * Criando a Express�o regular
   * Par�metros
   *  - caseSensitive: corresponde a flag "i" ignora UPPER e LOWER
   *  - dotAll: faz o ponto funcionar sobre quebra de linha e tab
   *  - multiLine: trata express�es em strings com mais de uma linha
   *  - unicode: trata caracteres UNICODE
   */

  RegExp regex = RegExp(r"[a-c]");

  /*
   * Executando a Express�o regular
   *  - allMatches: corresponde a utilizar a flag "g" busca global
   *  - hasMatch: retorna true ou false caso a Regex encontre dados
   *  - firstMatch: busca a primeira ocorr�ncia
   *  - stringMatch: busca a string da primeira ocorr�ncia
   */

  var match = regex.allMatches(texto);

  print(match);

}
```

#  <strong> Conte�do Abordado </strong>

 * Como Utilizar as Express�es Regulares no Dart
 * Utiliza��o dos Caracteres e Meta Caracteres
 * Conjuntos
 * Quantificadores
 * Grupos
 * Bordas
 * <strong>!! EXTRA !! - Algumas receitas para Express�es Regulares </strong>

#  <strong> Shorthand List </strong>

## <strong> Basics </strong>

| Shorts | Descri��o
| -      | -
| *      | Match preceding character 0 or more times
| +      | Match preceding character 1 or more times
| .      | atch any single character
| x\|y   | Match either 'x' or 'y'
| \      | Escape a special character
| b      | The character b
|abc     | The string abc

## <strong> Character Classes I </strong>

| Shorts | Descri��o
| -      | -
| \d     | Match a digit character
| \D     | Match a non-digit character
| \s     | Match a single white space character (space, tab, form feed, or line feed)
| \S     | Match a single character other than white space
| \w     | Match any alphanumeric character (including underscore)
| \W     | Match any non-word character

## <strong> Character Classes II </strong>

| Shorts | Descri��o
| -      | -
[abc]    | Match any one of the characters in the set 'abc'
[^abc]   | Match anything not in character set 'abc'
[\b]     | Match a backspace

## <strong> Assertions </strong>

| Shorts | Descri��o
| -      | -
| ^      | Match beginning of input
| $      | Match end of input
| \b     | Match a word boundary
| \B     | Match a non-word boundary
| ?=     | Lookahead
| ?!     | Negative lookahead

## <strong> Assertions II </strong>

| Shorts | Descri��o
| -      | -
| ?<=    | Lookbehind
| ?<!    | Negative lookbehind
| ?>     | Once-only subexpression
| ?()    | If then condition
| ?()\|  | If then else condition
| ?#     | Comment

## <strong> Quantifiers </strong>

| Shorts | Descri��o
| -      | -
| {n}    | Match exactly n occurrences of preceding character
| {n,m}  | Match at least n and at most m occurrences of the preceding character
| ?      | Match 0 or 1

## <strong> Special Characters I </strong>

| Shorts | Descri��o
| -      | -
| \cX    | Match control character X in a string
| \n     | Match a line feed
| \r     | Match a carriage return
| \t     | Match a tab
| \0     | Match a NULL

## <strong> Special Characters II </strong>

| Shorts | Descri��o
| -      | -
| \f     | Match a form feed
| \v     | Match a vertical tab
| \xhh   | Match character with code hh (2 hex digits)
| \uhhhh | Match character with code hhhh (4 hex digits)

## <strong> Flags </strong>

| Shorts | Descri��o
| -      | -
| g      | Global search
| i      | Case-insensitive search
| m      | Multi-line search
| y      | "sticky" search match starting at current position in target string

## <strong> Groups </strong>

| Shorts | Descri��o
| -      | -
| (x)    | Match 'x' and remember the match
| (?:x)  | Match 'x' but do not remember the match
| \n     | A back reference to the last substring matching the n parenthetical in the regex
# Java
I hope it helps !

## StringBuffer

`:StringBuffer ` Constrói um buffer de string inicializado com o conteúdo da string especificada. A capacidade inicial do buffer de string é 16 mais o comprimento do argumento de string.

```java
public StringBuffer(String str)
```
`:append `Acrescenta a string especificada a esta sequência de caracteres.

```java
StringBuffer buffer = new StringBuffer("select * ");
	buffer.append("from ");
	buffer.append(" Carro ");
	System.out.println(buffer);
```
RESULTADO: QUERY: select * from  Carro 

`:delete (int start, int end)` Remove os caracteres em uma substring desta sequência.
```java
	buffer.delete(0, 6);
	System.out.println(buffer);
```
RESULTADO: * from  Carro 


`:deleteCharAt(int index)` Remove o caractere na posição especificada nesta sequência.
```java
	buffer.deleteCharAt(0);
	System.out.println(buffer);
```
RESULTADO: elect * from  Carro

`:replace(int start, int end, String str)` Substitui os caracteres em uma substring desta sequência por caracteres na String especificada.
```java
StringBuffer buffer = new StringBuffer("select * ");
	buffer.append("from ");
	buffer.append("Carro");
	buffer.replace(14, 20, "Moto");
		
	System.out.println(buffer);
```
RESULTADO: select * from Moto

`:insert(int offset, String str)` Insere a string nesta sequência de caracteres.
```java
StringBuffer buffer = new StringBuffer("select * ");
	buffer.append("from ");
	buffer.append("Carro");
	buffer.replace(14, 20, "Moto");
	buffer.insert(18, " where");
	System.out.println(buffer);
```
RESULTADO: select * from Moto where

## DICA 

Como nos exemplos logo acima uso bastante para montagem de querys dinâmicas!

## Pattern - Regex

`:Pattern ` Uma expressão regular é uma sequência de caracteres que forma um padrão de pesquisa. Ao pesquisar dados em um texto, você pode usar esse padrão de pesquisa para descrever o que está procurando.
`:Pattern` - Define um padrão (para ser usado em uma pesquisa)
`:Pattern.compile()` - Pattern.CASE_INSENSITIVE - O primeiro parâmetro indica qual padrão está sendo pesquisado e o segundo parâmetro tem um sinalizador para indicar que a pesquisa não deve diferenciar maiúsculas de minúsculas. O segundo parâmetro é opcional.
O `:Matcher()` método é usado para procurar o padrão em uma string. Ele retorna um objeto Matcher que contém informações sobre a pesquisa realizada.
O `:find()` método retorna true se o padrão foi encontrado na string e false se não foi encontrado.

`:CANON_EQ`  Ativa a equivalência canônica.
`:CASE_INSENSITIVE` Ativa a correspondência que não diferencia maiúsculas de minúsculas.

```java
Pattern pattern = Pattern.compile("dummy", Pattern.CASE_INSENSITIVE);
Matcher matcher = pattern.matcher("Lorem Ipsum is simply dummy text of the printing and typesetting!");
		
	boolean matchFound = matcher.find();
		
	if (matchFound) {
		System.out.println("Achei");
	} else {
		System.out.println("Não Achei");
	}
```
RESULTADO: Achei

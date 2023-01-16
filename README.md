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

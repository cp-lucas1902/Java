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
		System.out.println("QUERY: " + buffer);
```
RESULTADO: QUERY: select * from  Carro 
	


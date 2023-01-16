# Java
I hope it helps !

## Modificadores de Acesso

Java controla o acesso a atributos e métodos através do uso dos modificadores de acesso. São eles :

`:public ` É o menos restritivo de todos. Atributos e métodos declarados como public

em uma classe podem ser acessados pelos métodos da própria classe, por classes

derivadas desta e por qualquer outra classe em qualquer outro pacote (veremos mais sobre pacotes e classes derivadas posteriormente).

`:protected` : Atributos e métodos definidos como protected são acessíveis pelos

métodos da própria classe e pelas classes derivadas.

`:private` : É o mais restritivo. Atributos e métodos declarados como private só podem ser acessados pelos métodos da própria classe.




```java
public String name = 'texto';
```

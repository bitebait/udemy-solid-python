# 📚 Meu repositório de estudos - SOLID Principles of Object-Oriented Design and Architecture

Repositório para praticar todo conteúdo absorvido durante o curso ["SOLID Principles of Object-Oriented Design and Architecture"](https://www.udemy.com/course/solid-principles-object-oriented-design-architecture) na plataforma Udemy.

​

*..algumas anotações sobre meu aprendizado durante o curso...*

* * *

## 📝 O princípio de responsabilidade única (SRP) 

O princípio de responsabilidade única (SRP) afirma que:

> “Uma classe deve ter um, e apenas um, motivo para mudar.”

Em outras palavras, cada componente do seu código (em geral uma classe, mas também uma função) deve ter uma e apenas uma responsabilidade. Como consequência disso, deve haver apenas uma razão para alterá-lo.

Alguns beneficios do SRP
- Facilidade de manutenção e evolução do código
- Código limpo e de fácil entendimento
- Facilidade para desenvolvimento de testes
- Redução do acoplamento
- Complexidade reduzida
- Coesão das classes

​

* * *
## 📝 O princípio aberto-fechado (OCP)

O princípio aberto-fechado (OCP) afirma que:

> “Entidades de software ... devem ser abertas para extensão, mas fechadas para modificação.”
> ... ou ...
> “Você deve ser capaz de estender um comportamento de uma classe sem a necessidade de modificá-lo.”

Você não deve precisar modificar o código que já escreveu para acomodar a nova funcionalidade, mas simplesmente adicionar o que você precisa agora.

Isso não significa que você não pode alterar seu código quando as premissas do código precisam ser modificadas, mas se você precisar adicionar novas funções semelhantes à presente, você não deve exigir a alteração de outras partes do código.

Em outras palavras significa que esta classe pode ter seu comportamento alterado com facilidade quando necessário, sem a alteração do seu código fonte. Essa extensão pode ser feita através de herança, interface e composição.

​

* * *
## 📝 O princípio de substituição de Liskov (LSP)

O princípio de substituição de Liskov (LSP) afirma que:

> “Funções que usam ponteiros ou referências para classes base devem ser capazes de usar objetos de classes derivadas sem saber.”
> ... ou ...
> “As classes derivadas devem ser substituíveis por suas classes base.”

Em (talvez) palavras mais simples, se uma subclasse redefine uma função também presente na classe pai, um usuário-cliente não deve estar notando nenhuma diferença no comportamento e é um substituto para a classe base.

Por exemplo, se você estiver usando uma função e seu colega alterar a classe base, você não deve notar nenhuma diferença na função que está usando. Dentre todos os princípios SOLID, este é o mais difícil de entender e explicar. 

​

![1*vXv5w1V6iHhQLM2GpVarEQ.png](https://miro.medium.com/max/690/1*vXv5w1V6iHhQLM2GpVarEQ.png)
*Image Source: https://medium.com/@tbaragao/solid-l-s-p-liskov-substitution-principle-3a31c3a7b49e*

​

* * *

## 📝 O Princípio de Segregação de Interface (ISP)

O Princípio de Segregação de Interface (ISP) afirma que:

> “Muitas interfaces específicas do cliente são melhores do que uma interface de uso geral.”
> ... ou ...
> "Clientes não devem ser forçados a depender de interfaces que eles não usam."

Nesse sentido, os princípios do SI nos dizem que uma classe deve ter apenas a interface necessária (SRP) e evitar métodos que não funcionam ou que não têm razão para fazer parte dessa classe. Esse problema surge, principalmente, quando uma subclasse herda métodos de uma classe base de que não precisa.
De forma mais clara, podemos dizer que o principio prega que uma interface não deve forçar uma classe a implementar coisas que ela não irá utilizar. Interfaces que tem muitos comportamentos (Interfaces gordas) geralmente se espalham pelo sistema trazendo complexidade e dificuldade de manutenção ao código.

​

* * *

## 📝  O Princípio de Inversão de Dependência (DIP)

O Princípio de Segregação de Interface (ISP) afirma que:

> “Abstrações não devem depender de detalhes. Os detalhes devem depender da abstração. Módulos de alto nível não devem depender de módulos de baixo nível. Ambos devem depender de abstrações.”
> ... ou ...
> "Dependa de abstrações e não de implementações."

Portanto, essas abstrações não devem ser dependentes de métodos de baixo nível, mas ambas devem depender de uma terceira interface. Para explicar melhor esse conceito, prefira pensar em uma espécie de fluxo de informações. 

Imagine que você tenha um programa que recebe um conjunto específico de informações (um arquivo, um formato, etc) e você escreveu um script para processá-lo. O que aconteceria se essas informações estivessem sujeitas a alterações? Você teria que reescrever seu roteiro e ajustar o novo formato. Perder a retrocompatibilidade com os arquivos mais antigos. No entanto, você pode resolver isso criando uma terceira abstração que pega as informações como entrada e as passa para os outros.

De uma forma objetiva o princípio nos faz entender que sempre devemos depender de abstrações e não das implementações, afinal de contas, as abstrações mudam menos e facilitam a mudança de comportamento e as evoluções do código.

## ** Oque é o SOLID? **
SOLID é um princípio utilizado pelos desenvolvedores de software. Seu objetivo é ajudar os programadores a escreverem códigos de qualidade, limpos, fáceis de serem reutilizados e de dar manutenção.

### SOLID significa
    [S] -> Single Responsibility Principle (Princípio da Responsabilidade Única)

    [O] -> Open/Closed Principle (Princípio do Aberto/Fechado)

    [L] -> Liskov Substitution Principle (Princípio da Substituição de Liskov)

    [I] -> Interface Segregation Principle (Princípio da Segregação de Interfaces)

    [D] -> Dependency Inversion Principle (Princípio da Inversão de Dependência)

## ** Agora aplicarei cada principio citado em alguns exemplos C#.**

## Single Responsibility Principal

Esse princípio diz que uma classe deve ter apenas uma responsabilidade, ele tem o objetivo de evitar colisões de código.

Para haver um melhor entendimento, criarei dois exemplos: um quebrando o princípio de SRP (`Single Responsibility Principle`) e outro aplicando-o.

## O exemplo a seguir é a violação do SRP, código feito em C# .net versão 7.0 

![Code](./img/codeSRP.js){ width=700, height=600, align=left }

No exemplo ascima o SRP é violado pelo fato de usar a classe *produto* para fazer a inclusão do mesmo no banco.

Com isso alguns pontos podem ser observados como má pratica:

* ** Falta de coesão ** - a classe não deve assumir responsabilidades que não são suas;
* ** testes automatizados ** - Dificuldades na implementação de testes automatizados pelo fato de toda camada de Repository e service estar na própria classe Produto.
* ** Dificuldades para reaproveitar o código. **

## Implementando do princípio SRP — Single Responsibility Principle.


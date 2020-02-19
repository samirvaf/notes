# SOLID -> https://github.com/EduardoPires/SOLID

 ### S - SRP: Single Responsibility Principle
 ### O - OCP: Open / Closed Principle
 ### L - LSP: Liskov Substitution Principle
 ### I - ISP: Interface Segregation Principle
 ### D - DIP: Dependency Inversion Principle


 Solid é um acrônimo dos cinco primeiros princípios da programação orientada a objetos e design de código identificados por Robert C. Martin (ou Uncle Bob) por volta do ano 2000.


 Os princípios **SOLID** devem ser aplicados para se obter os benefícios da orientação a objetos, tais como:
 - Seja fácil de se manter, adaptar e se ajustar às alterações de escopo;
 - Seja testável e de fácil entendimento;
 - Seja extensível para alterações com o menor esforço necessário;
 - Que forneça o máximo de reaproveitamento;
 - Que permaneça o máximo de tempo possível em utilização;
 

 ## SRP: Single Responsability Principle
 - Princípio mais simples e mais **importante** do SOLID;
 - Uma classe deve ter um, e apenas um motivo para ser modificada. Em outras palavras, cada classe deve ter apenas **uma** responsabilidade;
 - Exemplo: desacoplar uma classe Cliente, criar classes diferentes para conexão ao banco, serviços relacionados a cliente (adicionar, remover), deixar na classe principal apenas o "model" e uma validação para a própria classe;


 ## OCP: Open / Closed Principle
 - Entidades de software (classes, módulos, funções) devem estar abertas para extensão, mas fechadas para modificação;
 - Exemplo: uma classe conta com uma função Debitar que se comporta de forma diferente dependendo do tipo de conta. O correto é extender de uma classe abstrata Conta e sobreescrever o método Debitar;

## LSP - Liskov Substitution Principle
- Uma classe base deve poder ser substituída pela sua classe derivada;
- Tomar cuidado com as abstrações, exemplo -> Quadrado é um Retângulo, logo poderíamos extender classe quadrado da classe base retângulo, porém não é bem assim, para garantirmos um quadrado precisamos sobreescrever as propriedades da classe base (altura e largura devem ser iguais). Isso pode levar a diversos problemas;
- Em tais casos, escrever classes separadas;

## ISP - Interface Segregation Principle
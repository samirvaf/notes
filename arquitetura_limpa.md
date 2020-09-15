# Arquitetura Limpa


## Capítulo 1 - O que são design e arquitetura?

- Os dois termos são utilizados, normalmente design se refere a detalhes de baixo nível enquanto a arquitetura se preocupa com a descrição alto nível porém não existe diferença entre eles, são parte do mesmo todo e não existe uma linha que os separa claramente.
- O objetivo da arquitetura de software é minimizar os recursos humanos necessários para construir e manter um determinado sistema.
- A única maneira de seguir rápido é seguir bem, manter sempre a autoconfiança sob controle, não cair em ciladas do tipo: "depois posso voltar e arrumar esse código, nesse momento o mais importante é liberar o release logo".
- Desenvolvedores podem achar que a resposta para resolver problemas de um sistema que declinou a produtividade de toda uma equipe a zero é reescrever todo o sistema, na realidade o que é preciso é uma mudança na mentalidade, ou o novo sistema está fadado ao mesmo destino.

## Capítulo 2 - Um conto de dois valores

- Nesse capítulo o autor faz uma análise sobre a importância da arquitetura levantando em conta dois valores importantes, funcionalidade e capacidade de mudança.
- Infelizmente a maior parte dos desenvolvedores prioriza a funcionalidade ao invés de uma boa arquitetura, um argumento simples que demostra como essa atitude está incorreta é: se você me der um programa que não funciona mas que seja fácil de ser modificado eu posso fazê-lo funcionar e mantê-lo funcionando por muito tempo, em contrapartida se você me der um programa que funciona porém que seja difícil de ser modificado, o programa não funcionará assim que os requisitos mudarem.
- Colocar a arquitetura em segundo plano parte do princípio que a funcionalidade é urgente, gerentes de negócio querem o software funcionando o quanto antes, porém a **importância** está acima da **urgência** (matriz de Eisenhower), e cabe a equipe de desenvolvimento lutar para garantir que a arquitetura seja entendida como prioridade considerando o longo prazo, vida útil do software.
- Se a arquitetura vier por último, então o sistema ficará cada vez mais caro para se desenvolver e, por fim, a mudança será praticamente impossível para parte ou para todo o sistema.

## Capítulo 3 - Panorama do paradigma

- Neste breve capítulo o autor apresenta os três principais paradigmas da programação com um breve histórico de casa e uma frase que resume bem cada paradigma, são essas:
- A programação estruturada impõe disciplina sobre a transferência direta do controle. (Declarações goto)
- A programação orientada a objetos impõe disciplina sobre a transferência indireta do controle. (Polimorfismo)
- A programação funcional impõe disciplina sobre a atribuição. (É possível alterar o valor de variáveis apenas em situações muito específicas)
- Observar que cada paradigma **remove** capacidades do programador. Cada um impõe algum tipo de disciplina adicional com intenção negativa.

## Capítulo 8 - OCP: O princípio aberto/fechado

- Um artefato de software deve ser aberto para extensão, mas fechado para modificação.
- O OCP é uma das forças motrizes por trás da arquitetura de sistemas. Seu objetivo consiste em fazer com que o sistema seja fácil de estender sem que a mudança cause um alto impacto. Para concretizar esse objetivo, **particionamos** o sistema em componentes e **organizamos** esses componentes em uma hierarquia de **dependência** que **proteja** os componentes de nível mais alto das **mudanças** em componentes de nível mais baixo.
- Para que componente A seja protegido das mudanças no componente B, o componente B deve depender do componente A.

## Capítulo 9 - LSP: O Princípio de Substituição de Liskov

- Tomar cuidado com tratamento de "casos especiais" espalhando "ifs" dentro do código.
- O arquiteto deve criar um mecanismo configurável, uma espécie de mapping que deve lidar com casos especiais de forma invisível e centralizada.
- O LSP pode, e deve, ser estendido ao nível da arquitetura. Uma simples violação da capacidade de substituição pode contaminar a arquitetura do sistema com uma quantidade significante de mecanismos extras.


# Ruby Study Notes


## Chapter 16 - Mixins
> Preciso utilizar o código de um método e/ou constantes de uma classe em outra completamente não relacionadas


Utilizar o conceito de mixins que se resume em:

- Exportar o código que será utilizado para um módulo
- Incluir o módulo nas classes que irão utilizá-lo
- Logo após a definição da classe - **include nome_do_modulo**
- Ainda é possível transformar os métodos do módulo em métodos da classe (pesquisar)

## Chapther 17 - Code blocks
> Pequena revisão sobre code blocks

Podemos usar code blocks para:

- Criar iterators **(pesquisar syntax)**, métodos que recebem um code block e chamam o mesmo para cada item de alguma coleção
- Enumerable pode ser incluído nas classes, é um módulo com várias utilidades que podem ajudar em diversos aspectos e.g. find e find_all (pesquisar)
- **Não confundir com Enumerator** que possui outras utilidades como .count e .sort
- Ao criar iterators sempre considerar que não possuimos controle sob o que é passado no code block, ou seja, não confiar demais
- Para casos críticos que não se pode prever se uma exception pode ocorrer durante a iteração utilizar **begin/ensure**

## Chapter 18 - Execute around a block
> O que é a técnica execute around?

Podemos criar métodos que tratam cenários em que precisamos que algo execute antes e/ou depois da lógica do método em si. Bons exemplos são loggings.
- O método deve receber um code block, executar algo antes do yield e executar algo após o yield
- É possível tratar exceptions de forma generalista
- Podemos usar execute around para inicializar objetos de forma mais legível (pesquisar)

## Chapter 19 - Save blocks to execute later
> Como utilizar code blocks para executar pedaços de código no momento certo

Podemos criar metódos que recebem code blocks para inicializar determinados parâmetros, criar listeners.
- Code blocks com parâmetros explícitos devem ser utilizados
- Lembrar da diferença entre o uso de lambda e Proc.new (pesquisar)
- Tomar cuidado com o escopo em torno do code block já que ele suga todas as variáveis enquanto estiver ativo, lembrar do exemplo de um array com muitos elementos

## Chapter 20 - Hooks
> Como utilizar hooks para manter seu programa informado

Podemos criar hooks para capturar informação sobre o nosso programa que pode ser muito útil para tratar casos específicos
- self.inherited(subclass) é disparado sempre que a classe em que a hook é definida é herdada, muito útil para manter uma lista de subclasses e utilizar isso para chamar um método em comum a todas as subclasses, cada uma com uma implementação diferente. Exemplo um reader de documentos em que cada subclasse é capaz de ler uma extensão diferente
- self.included(host_class) é a versão para módulos, o principal uso dessa hook é quando queremos adicionar instance methods **e** class methods a uma determinada classe sem precisar criar dois módulos diferentes e chamar include e extend
- at_exit é um hook chamado logo antes do programa encerrar, ele recebe um bloco de código e o executa. Podemos definir vários 'at_exit', porém é importante lembrar que é executado na ordem 'last-in/first-out'
- Para utilizar hooks de forma efetiva precisamos saber **examente quando eles são chamados**
- Existem vários hooks, esses são apenas alguns exemplos dos mais usados, pode ser interessante pesquisar

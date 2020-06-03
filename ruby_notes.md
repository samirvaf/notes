# Ruby study notes

> Preciso utilizar o código de um método e/ou constantes de uma classe em outra completamente não relacionadas


Utilizar o conceito de mixins que se resume em:

- Exportar o código que será utilizado para um módulo
- Incluir o módulo nas classes que irão utilizá-lo
- Logo após a definição da classe - include nome_do_modulo
- Ainda é possível transformar os métodos do módulo em métodos da classe (pesquisar)

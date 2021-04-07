# Orientação a objetos em .NET
## DIO com o professor: Bruno de Campos Dias

Paradigmas da programação: Cada paradigma surgiu de necessidade diferente. Dado isso, cada um apresenta maiores vantagens sobre os outros dentro do desenvolvimento de determinado sistema. Sendo assim, um paradigma pode oferecer técnicas apropriadas para uma aplicação especifica. Entre eles, estão a programação orientada a objetos - POO e a Programação Estruturada – PE.

Programação Estruturada: Tem como principal características sua interpretação linha por linha, em pequenos trechos de códigos, podendo eles não estar em uma ordem específica. Há três tipos de estruturas básicas para o navegador peço código: Sequência, Seleção e a Repetição.

Seqüência: São comandos a serem executados de cima para baixo, linha a linha, do pragrma de forma seqüencial.
Seleção: Seqüências que só deve ser executadas se uma condição for satisfeita(ex. IF- else, switch e comandos parecidos).
Repetições: Seqüência que devem ser executadas repetidamente até uma condição for satisfatória (for, while, do-while etc).

Programação Orientada a Objeto: O POO é baseado no conceito de ‘objetos’, que podem conter dados na forma de campos (atributos ex. carro= cor modelo portas) e códigos, na forma de procedimentos (métodos ex. carro= as ações correr, estacionar etc). Uma característica é que um procedimento de objeto pode acessar, e geralmente modificar, os campos de Dados do Objeto com a qual eles estão associados e cada um é de receber processar e enviar dados, podendo ser visto como uma “maquina independente”

A importância da POO é simples e direta. Tudo em .NET é objeto. Mesmo os tipos de dados mais simples são considerados objetos, já estes também contém métodos e propriedades. Implicitamente, todo e qualquer tipo ou objeto em .NET possui um ancestral comum.

O que são?
Classes: Pode ser considerado como se fosse um molde para o objeto, contendo dentro de si as principais informações para a sua criação. Define os atributos (características) e métodos(ação) comuns que serão compartilhados por um objeto.
 
Objetos: Considera-se um objeto tudo aquilo que em geral possui atributos, comportamentos e um estado. A classe em si é um conceito abstrato, como molde, que se torna concreto e palpável através da criação de um objeto.
Na programação o objeto é uma instanciação (criação a partir) de uma classe. Para criarmos ou “instanciarmos” objetos de uma determinada classe, utilizamos o operador new.
Ex: 
1  Produto obj = new Produto();

Visibilidade: A visibilidade é importante para a proteção do código e suas funcionalidades, define quem pode alterar cada dado dos trechos de código em três principais níveis: Pública – Representada pelo símbolo “+”, Privada - Representada pelo símbolo “-”, Protegida - Representada pelo símbolo “#”.
Como ela se comporta:
Publica – Sem limitação de acesso.
Protegida Interna – Acesso limitado à própria classe, às classes derivadas e ao próprio assembly.
Protegida – Acesso limitado à própria classe, as classes derivadas.
Interna – Acesso limitado ao próprio assembly.
Privado – Acesso limitado á própria classe.

É o que chamamos de encapsulamento, que impede o vazamento de escopo. Esse encapsulamento de atributos e métodos impede o chamado vazamento de escopo, onde um atributo ou método é visível por alguém que não deveria vê-lo, como outro objeto ou classe.
Tipos por Valor C#
O C# tem duas grandes categorias de tipos: por valor e por referencia. Os tipos por valor são gerenciados diretamente e têm as seguintes características principais: Todos os tipos de dados numéricos. Não precisam ser inicializados com o operador new. A variável armazena o valor diretamente.
A atribuição de uma variável a outra copia o conteúdo, cirando efetivamente outra cópia da variável. Não podem conter valor null. Exemplos de variáveis desse tipo são doubles, floats e char.
Temos variáveis de tipo inteiro (integers) têm sempre o mesmo significado, independentemente da implementação.
Os números de ponto flutuantes são bastante convencionais, as operações de ponto flutuante não geram erros.
Caracteres: Em C#, todos os caracteres (char) não sendo compatível a com inteiro mas são armazenados no padrão Unicode e usam 16bits por caracter. O uniocode permite armazenar os caracteres de todas as línguas vivas (grego,japonês, chinês etc) não vivas (sânscrito). 
Tipos por referência: Um tipo por referencia armazena uma referencia a seus dados. Os tipos de referencia incluem o seguinte: Duas variáveis poderá conter a referencia a um mesmo objeto. Operações em uma pode afetar a outra.
Todas as matrizes, mesmo que seus elementos sejam do tipo de valor. Exemplos de tipos por referencia: Strings, classes e arrays.
Strings: Semelhantes ao char, strings são variáveis do tipo texto. São uma sequencia de caracteres, geralmente utilizada pra representar palavras, frases ou textos de um programa.
As strings são consideradas imutáveis e não podem ser alteradas depois de criadas. Quando vocÊ efetua uma operação qualquer, como ex. concatenar um caracter, você na verdade esta criando outra string e descartando a anterior.
Classes: São definidas por usuário e correspondem a uma class. As classes são sempre derivadas de object e podem conter capôs, métodos e propriedades. Uma classe pode derivar de uma única outra classe, e também de várias interfaces.
Array: É uma lista de valores onde todos os valores no grupo são referenciados pelo nome da matriz e o índice atribuído ao valor especifico na matriz.
Ponteiro: Um apontador é um tipo de dado de cujo valor se refere diretamente a outro valor alocado em outra área da memória, através de seu endereço.
Métodos: determinam o comportamento dos objetos de uma classe e são capazes de controlar o estado da estância. São funções que realizam tarefas. Eles podem ou não retornar valores, e podem ou não receber parâmetros.
O envio de mansagens (chamada dos métodos) pode alterar o estado de um objeto. Esse método tem como difundidos os Getters, os Setters e o Construct.
Os Getters ou métodos acessores solicitam o acesso a informação de um determinado produto sem dar acesso diretamente a ele, colocando ali uma barreira de proteção para os dados.
Ex. public int código{ 
get{ return código;}
set { código = value;}}

Os Setters ou métodos modificadores enviam o pedido de alteração de uma determinada informação de um objeto sem que se altere diretamente o mesmo.

A função Construct ou método construtor é inicializar ou dar forma á classe. È nele que indicamos os valores dos campos de uma classe. Esses valores podem ser internos (no código) ou esternos (passando por parâmetros).
As regras para definição de um construtor são:
•	O construtor deve ter o mesmo nome da classe;
•	Não tem tipo de retorno;
•	É executado apenas um, apenas uma vez, no momento da criação do objeto;
•	Não pode ser chamdo diretamente;
•	Deve ser”public”;

Propriedade e Eventos
Uma forma mais inteligente de fazer implementação de campos em classes são as propriedades.
Propriedades consistem em um par de métodos “get” e “set” que respectivamente servem para recuperar e atribuir o valor do Campo. Para cada método existe uma variável e dentro da classe que armazena o valor da propriedade.
Eventos São mensagens que a classe dispara para uma determinada situação, para que o evento funcione é necessário que um método seja escrito pra ser executado quando ocorrer o evento. A classe apenas fica sabendo que existe esse método em tempo de execução. Ex. quando passamos o mouse vemos o evento. Para que o mecanismo dos eventos funcione, é necessário usar um tipo de estrutura chamada Delegate, uma variável que guarda o endereço de uma função. Assim, quando o evento é disparado, essa variável chama a função associada a ela.




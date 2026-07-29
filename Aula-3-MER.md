# MER

Este documento descreve o que é o MER e como e porque utilizá-lo.


## O que é o MER?

O MER é a sigla para Modelo e Entidade Relacionamento. Ele é, basicamente, um **desenho** representando o nosso banco de dados e como nossas **entidades** (que são nosssas tabelas depois) se ligam e se **relacionam**.


## Porque preciso fazer esse desenho? Não é mais fácil só fazer o banco?

É sim possível criar o banco sem fazer o MER. Porém, o MER faz parte do **planejamento** do nosso banco de dados. É como fazer um prédio sem desenhar a planta antes. É possivel, mas garanto que você não ia querer morar nele.
Ao fazer o MER, nós estamos cuidando para que nosso banco saia exatamente como necessário, sem mais nem menos. Assim evitamos retrabalho lá na frente.

## Onde e como eu posso fazer este desenho?

O MER pode ser feito em qualquer plataforma ou programa que permita desenhar, existem programas específicos para trabalhar com ele, mas você pode usar o Canva, Photoshop, Paint ou até mesmo uma folha de papel. No entanto, o mais recomendado é utilizar programas específicos, por exemplo: O BrModelos:

Link para o BrModelos: https://www.brmodeloweb.com/

## Qual o passo a passo para desenharmos?

Antes de fazermos o MER precisamos primeiro ter definido quais as **entidades** (tabelas) e ter feito o **dicionário de dados** (aquela lista que define os campos e os tipos de dados destes campos). Então, podemos começar desenhando as entidades no MER. Elas são representadas por *retângulos* com o nome dentro.
Os atributos que nós planejamos anteriormente para essas **entidades** também devem aparecer no desenho (assim psabemos como construir as tabelas depois só de olhar o desenho). Eles são representados por bolinhas sem fundo, ou "brancas".

**ATENÇÃO**: Se um atributo for um uma **chave primária** ele será representado por uma bolinha preenchido, ou "preta".

Ambas devem estar ligadas às entidades (retângulos) por **linha**.
Para podermos criar as **chaves estrangeiras**, que são os campos que lígam uma tabela em outra, normalmente pegando emprestado a **chave primária** de outra tabela. Não usamos "bolinhas" para representá-las, e sim **losangos** com linhas ligando as entidades em questão. Dentro deste losango, damos um título para relação. Por exemplo, um **cliente** "compra" uma **bicicleta**.
Um passo importante para entender os relacionamentos é a **cardinalidade**. Ela nos ajuda a entender quantos registros dentro de uma tabela conseguem se relacionar com quantos de outra tabela. Confuso?
Pense só: Em quantas vendas um bicicleta pode estar? Uma só. Note que eu usei a palavra "pode".
Agora, uma venda pode ter quantas bicicletas? Várias, correto? 
Um cliente pode fazer várias compras, quantas ele quiser. Pode também não fazer nenhuma.


### Tipos de cardinalidades:

* **(0,1)** - Pode não participar de nenhum relacionamento ou participar de apenas um. 
*Exemplo: Um funcionario pode ou não ter um carro da empresa.*

* **(1,1)** - Deve participar de exatamente um relacionamento.
*Exemplo: Todo empréstimo deve estar associado a um único cliente.*

* **(0,N)** - Pode não participar de nenhum relacionamento ou participar de várias.
*Exemplo: Um cliente pode nunca fazer um empréstimo ou fazer vários ao longo do tempo.*

* **(1,N)** - Deve participar de pelo menos um relacionamento, mas pode participar devárias.
*Exemplo: Um empréstimo deve conter pelo menos uma bicicleta, mas pode conter várias.*

* **(N,N)** - Ambos os lados podem participar de vários relacionamentos. Também é chamado de relacionamento muitos-para-muitos.
*Exemplo: Um aluno pode cursar várias discíplinas, e uma discípina pode ter vários alunos.*

### Resumindo: 

* **0** = Opicional (pode não existir) 
* **1** = Obrigatório (deve existir)
* **N** = Muitos (vários)


Então: 

* **(0,1)** → Opcional e no máximo um.
* **(1,1)** → Obrigatório e exatamente um.
* **(0,N)** → Opcional e vários.
* **(1,N)** → Obrigatório e vários.
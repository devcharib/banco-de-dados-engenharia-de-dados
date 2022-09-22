# banco-de-dados-engenharia-de-dados
O Papel dos Bancos de Dados SQL e NoSQL
## Banco de Dados SQL

  Bancos de dados relacionais usam a convenção de bases de dados que contem tabelas, onde cada coluna representa um campo e cada linha representa um registro. Tabelas podem ser relacionadas ou ligadas umas com as outras, com o uso do conceito de chaves estrangerias ou colunas em comum. Em um nível mais abstrato tabelas representam entidades, como usuários, produtos, empresas, entre outras. Esta abstração é muito útil para se desenhar o esquema do banco de dados onde objetos do mundo real precisam ser mapeados para a base de dados (HADJIGEORGIOU, 2013).

  Um importante aspecto do design dos bancos de dados relacionais se refere a sua normalização.

A normalização de um banco de dados é dividida em três formas idealizadas por Codd, E.F em 1970 em seu livro “A Relational Model of Data for Large Shared Data Banks”, abaixo segue um breve resumo de cada forma:

- **Primeira Forma Normal** (ou 1FN) A normalização para a primeira forma normal elimina grupos repetidos, pondo-os cada um em uma tabela separada, conectando-os com uma chave primária ou estrangeira.

- **Segunda Forma Normal** (ou 2FN) requer que não haja dependência funcional não trivial de um atributo que não seja a chave, em parte da chave candidata.

- **Terceira Forma Normal** (ou 3FN) requer não haver dependências funcionais não triviais de atributos que não sejam chave, em qualquer coisa exceto um super-conjunto de uma chave candidata.

## Banco de Dados NoSQL
  
  Bancos NoSQL possuem quatro grandes variedades, as quais iremos abordar com mais detalhes nos próximos capítulos, são ela s; orientados a documentos, orientados a colunas, “key-value” e orientados a grafos. Cada uma destas variedades possui a sua própria maneira de armazenar os dados, os bancos relacionais têm sido escolhidos para todos os tipos de soluções e cenários analíticos, porém bancos NoSQL possuem diversas vantagens em vários cenários específicos, por exemplo, um banco orientado a grafos normalmente seria usado em um cenário onde um banco orientado a documentos não apresentaria o desempenho ou modelo apropriado (HOBERMAN, 2014).
  
  Bases NoSQL possuem um foco menor na integridade dos dados e um foco maior no desempenho e na disponibilidade seguindo o acrônimo BASE Basically Available (Basicamente Disponível), “Soft-state”, Eventual consistency (Consistente eventualmente) (HOBERMAN, 2014).

 - Basicamente Disponível: Há uma resposta para cada query realizada, porém esta resposta pode informar que ocorreu um erro na execução da query ou ate mesmo que a informação retornada pode estar defasada, pois ainda está passando por uma mudança de estado. Um exemplo deste cenário: um vendedor de livros que ao consultar o inventário da livraria obtém a informação de quantos livros ela possui, porém também recebe um alerta informando que a informação não foi totalmente atualizada nas ultimas 24 horas podendo assim estar defasada.
  
 - “Soft-state”: significa que os bancos de dados NoSQL trabalham atualizando continuamente os dados com cada atualização realizada, o que tornaria a informação de nosso exemplo anterior em momentaneamente inconsistente, pois já pode ter ocorrido uma venda de um livro que não foi completamente atualizada em todo o banco.
  
 - Eventualmente consistente: Consistência significa que o dado atual reflete qualquer mudança que possa ter ocorrido ate aquele momento no tempo. Bases NoSQL eventualmente se tornam consistentes, porém somente quando param de receber novos dados para inserção ou atualização. Em nosso exemplo os dados do inventário podem estar consistentes minutos ou horas após a compra de um livro.
 
 
 
 
 
 
 > FONTE: https://medium.com/neogrid/nosql-x-bancos-relacionais-d06d0564e32
  

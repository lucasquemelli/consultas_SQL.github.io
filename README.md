# consultas_SQL.github.io
Este é um repositório para comandos avançados de SQL sobre consultas.

# Banco de dados

- Para sabermos quantas chaves estrangeiras uma tabela possui, podemos clicar no item "Foreign keys". 

![image](https://user-images.githubusercontent.com/81119854/130450097-d42142c2-d806-49b5-9624-934a874f98c5.png)

- Para sabermos de que chave se trata, podemos clicar sobre cada chave:

![image](https://user-images.githubusercontent.com/81119854/130450233-f2dcaf6d-baa3-4213-85bc-8ab1f82963a5.png)
![image](https://user-images.githubusercontent.com/81119854/130450302-c0c7ffbf-513a-44b3-b383-a6c8afd888b2.png)

- Podemos gerar gerar um esquema visual de uma tabela (e das tabelas a ela relacionadas) a partir de "Database -> Reverse Engineer".

![image](https://user-images.githubusercontent.com/81119854/130451965-d8c6a7bc-e2aa-4246-b962-22ce28d8e4c0.png)
![image](https://user-images.githubusercontent.com/81119854/130452017-87d08510-0f22-41e9-9294-4bc2303c9b79.png)
![image](https://user-images.githubusercontent.com/81119854/130452078-5d12e04e-bd35-47b8-bd50-df0813fe1a7f.png)

- Podemos diminuir o zoom e movimentar as tabelas de acordo com a necessidade:

![image](https://user-images.githubusercontent.com/81119854/130452488-1ae458aa-e050-4b9b-8233-36f815d3d6ea.png)

![image](https://user-images.githubusercontent.com/81119854/130452818-bc755a7f-3537-472b-b8d5-37d927587c6a.png)

- Podemos clicar na linha de conexão entre as tabelas para ver qual a relação entre elas:

![image](https://user-images.githubusercontent.com/81119854/130453268-07e3580f-9b02-4832-9983-e9c2fae32cf8.png)

![image](https://user-images.githubusercontent.com/81119854/130453423-d28731e4-7149-4f77-abcb-1890368d47f9.png)

# Básico de consultas

- Aplicando consultas condicionais:

![image](https://user-images.githubusercontent.com/81119854/130487284-effe2c36-f717-43e4-8224-d066d8494fba.png)

![image](https://user-images.githubusercontent.com/81119854/130487492-e9d0a859-4a2a-4fe8-94bc-907083f1ed44.png)

- Aplicando NOT no comando acima:

![image](https://user-images.githubusercontent.com/81119854/130488364-b206e167-9d57-429b-b67f-48b13eebc960.png)

![image](https://user-images.githubusercontent.com/81119854/130488473-d42b9ab1-1533-482f-9386-0c1e97c0fb34.png)

![image](https://user-images.githubusercontent.com/81119854/130488810-470e197c-8d74-4ae5-87b1-3ce606f4e8d6.png)

- Também podemos aplicar condições que expressem um conjunto:

![image](https://user-images.githubusercontent.com/81119854/130489146-75c0a31b-b426-4b09-b316-993ef02843fd.png)

- Mesclando condições de diferentes campos:

![image](https://user-images.githubusercontent.com/81119854/130489663-579f1e1c-94dc-4312-812e-779758444399.png)

![image](https://user-images.githubusercontent.com/81119854/130490258-0ce1ef50-2c94-47af-92eb-fafaa88acd55.png)

- Usando o comando LIKE:

![image](https://user-images.githubusercontent.com/81119854/130491855-22ea6c6a-ea00-4359-b503-18681555cd96.png)

- Exercício: Quantos clientes possuem o último sobrenome Mattos?

Para responder esta a questão, devemos considerar que o último sobrenome é o item desejado. Assim, ao usarmos o comando LIKE, o símbolo '%' deve indicar que há conteúdo na frente do sobrenome, mas não há nada atrás.

![image](https://user-images.githubusercontent.com/81119854/130492521-c129fef2-29ac-454a-9fd9-5da9b77919db.png)

# Apresentação dos dados de uma consulta

- Utilizamos DISTINCT para selecionarmos valores que não se repetem. Por exemplo, ao escolhermos os campos EMBALAGEM e TAMANHO da tabela de produtos, vários valores são apresentados: 

![image](https://user-images.githubusercontent.com/81119854/130494498-ae790e16-513e-4b1b-b3a4-eb0a75b0e384.png)

Entretanto, ao utilizarmos o comando DISTINCT, os valores exibidos serão aqueles que a combinação entre EMBALAGEM e TAMANHO não é repetida:

![image](https://user-images.githubusercontent.com/81119854/130494671-1d05267e-1657-45a9-aa03-d73323455ccc.png)

- Também podemos utilizar o comando DISTINCT com alguma outra condição:

![image](https://user-images.githubusercontent.com/81119854/130495043-816f1600-95b8-4428-a913-52fa24abb6b5.png)

- Se aumentarmos os campos de busca, o número de combinações aumenta e, consequentemente, aumentam as opções apresentadas como resultado:

![image](https://user-images.githubusercontent.com/81119854/130495421-3b780d79-e0d3-439f-aa3c-1a668f2ae0b0.png)

Exercício: Quais são os bairros da cidade do Rio de Janeiro que possuem clientes?

![image](https://user-images.githubusercontent.com/81119854/130495856-9d7e60f6-8070-431d-a805-ab9f9de8a429.png)

- Limitando o número de componentes a serem exibidos em uma tabela:

![image](https://user-images.githubusercontent.com/81119854/130500998-9955f732-2b1f-438e-9744-34b95aa148e4.png)

Podemos, também, limitarmos a exibição de valores a partir de uma posição e estabelecendo uma quantidade de registros a serem exibidos. Por exemplo, ao utilizarmos 'LIMIT 2,3', estamos estabelecendo que queremos começar a exibir a partir do valor na posição 2 (inicia-se a contagem em 0) e queremos exibir 3 valores:

![image](https://user-images.githubusercontent.com/81119854/130501597-c6a9517b-1252-4e1b-9505-4b5bfaed9ac1.png)

A partir da posição zero:

![image](https://user-images.githubusercontent.com/81119854/130502035-b2c73bcf-2490-413d-a81e-7004e3eeb04a.png)

- Exercício: Queremos obter as 10 primeiras vendas do dia 01/01/2017. Qual seria o comando SQL para obter este resultado?

Para resolvermos esta questão, primeiramente, devemos identificar qual a tabela que contém as informações desejadas. Neste caso, é a tabela "notas_fiscais":

![image](https://user-images.githubusercontent.com/81119854/130502439-8f30c363-cb82-45e6-a44e-01e997065c87.png)

Assim, podemos executar os comandos necessários:

![image](https://user-images.githubusercontent.com/81119854/130502822-6c67ae30-e46f-4a8b-902a-4cf2b425a78a.png)

- Para fazer ordenação dos registros de uma tabela, fazemos:

![image](https://user-images.githubusercontent.com/81119854/130522316-0d5d17a9-7ac7-49f3-8c8f-d99a0b10d58f.png)

Note que, ao utilizar ORDER BY, os preços foram ordenados em ordem crescente. Para selecionar os valores em ordem decrescente, fazemos:

![image](https://user-images.githubusercontent.com/81119854/130522570-3908540a-e531-47a7-85de-34caee7c6b68.png)

- Também podemos fazer ordenações por strings (ordem alfabética):

![image](https://user-images.githubusercontent.com/81119854/130522735-1e1b39ea-c73f-4f31-b4bf-ad855e9e0df7.png)

Utilizando o comando DESC:

![image](https://user-images.githubusercontent.com/81119854/130522850-4272f58e-2774-47ff-b2eb-8348d11d5b0d.png)

- Podemos ordenar strings de forma composta:

![image](https://user-images.githubusercontent.com/81119854/130523071-91c7e36c-3737-4d8c-999c-16cff6278119.png)

Note que, ao colocarmos o campo EMBALAGEM antes do campo NOME_DO_PRODUTO, primeiro segue-se o critério alfabético para o campo EMBALAGEM. Após o fim de um critério alfabético do primeiro campo (nesta caso: Garrafa), inicia-se o próximo critério do primeiro campo. 

Também podemos mesclar os critérios de seleção:

![image](https://user-images.githubusercontent.com/81119854/130523602-ca239083-a73d-4a07-b8d1-f1893a21dd79.png)

- Qual (ou quais) foi (foram) a(s) maior(es) venda(s) do produto “Linha Refrescante - 1 Litro - Morango/Limão”, em quantidade? (Obtenha este resultado usando 2 SQLs).

O primeiro SQL foi para determinar o código do produto a partir do nome fornecido no enunciado da questão:

![image](https://user-images.githubusercontent.com/81119854/130524155-4324ad15-f5b6-4791-800e-35dbab819ccb.png)

O segundo SQL foi para determinar as maiores vendas do produto mencionado:

![image](https://user-images.githubusercontent.com/81119854/130524546-e5cec800-0757-48af-907c-f76450a03ff1.png)

- Podemos agrupar respostas. Por exemplo, para o limite de crédito dos clientes, temos:

![image](https://user-images.githubusercontent.com/81119854/130525472-4be45478-e59a-46b0-ad43-fd47879081c8.png)

![image](https://user-images.githubusercontent.com/81119854/130527376-f3bbb38c-bbb5-4c16-953f-efa083e4883e.png)

Também podemos agrupar o preço por embalagem:

![image](https://user-images.githubusercontent.com/81119854/130527655-aa0a8b56-8089-4ffa-ae37-f56f7c5c2104.png)

Para agrupar pelo valor máximo do preço, fazemos:

![image](https://user-images.githubusercontent.com/81119854/130527800-fdf35d4d-06fa-464e-9477-ae4561d61953.png)

- Podemos utilizar a função COUNT para contarmos o número de tipos de embalagens:

![image](https://user-images.githubusercontent.com/81119854/130528068-6c47c36f-9e8a-4c4f-9ff7-0f1ef3313550.png)

- Limite total de créditos de clientes por bairro:

![image](https://user-images.githubusercontent.com/81119854/130528344-21fdbdb7-d850-43f2-bfc0-ff1b1e2b5b3d.png)

- Podemos agrupar o limite total de créditos de clientes por bairros de uma cidade específica:

![image](https://user-images.githubusercontent.com/81119854/130528499-a09c0934-142d-43f2-94f7-19fef82b846f.png)

- Podemos agrupar por bairros de estados diferentes:

![image](https://user-images.githubusercontent.com/81119854/130528763-36f6b803-f4a5-4aff-b846-a6ad10717bd6.png)

- Além de agrupados, os dados podem também estar ordenados:

![image](https://user-images.githubusercontent.com/81119854/130529015-1d5d2c2e-706e-496b-b567-54007b37676f.png)

- Exercício: Quantos itens de venda existem com a maior quantidade do produto '1101035'?

![image](https://user-images.githubusercontent.com/81119854/130615687-1efbcbab-ef13-4247-88aa-2ec1eccdef84.png)

- Having: se aplica a um resultado de um SELECT que é grupado.

![image](https://user-images.githubusercontent.com/81119854/130616875-014869d0-1735-4815-99fc-62210269764d.png)

- Não precisamos aplicar a condição having apenas para a função que utilizada, como no caso acima. Também podemos utilizar novas funções:

![image](https://user-images.githubusercontent.com/81119854/130618079-d4bc6769-fffd-4060-a2d3-8ebc1552e9a1.png)

- Também podemos aplicar a condição AND após uma condição HAVING:

![image](https://user-images.githubusercontent.com/81119854/130618347-8c9018b5-7b91-4ff7-8163-9eff6d200c5d.png)

- Exercício: Quais foram os clientes que fizeram mais de 2000 compras em 2016?

![image](https://user-images.githubusercontent.com/81119854/130624432-71c969c2-3455-4093-8ff0-e9862c43f9f3.png)

- Podemos utilizar CASE para classificar resultados. A utilização de CASE acontece de forma que um resultado é apresentado se ele atender certas condições. Abaixo um exemplo:

![image](https://user-images.githubusercontent.com/81119854/130628850-60edc959-fd19-469f-873a-f69b38242f63.png)

- Podemos utilizar CASE para agrupar por embalagens. Para isso, fazemos:

![image](https://user-images.githubusercontent.com/81119854/130631305-7d04e33a-54cf-468b-89e0-4efb69be56ba.png)

Repare no código acima que o mesmo tipo de embalagem pode apresentar 'status de preço' diferente. Isso acontece porque existem embalagens de um certo tipo que fazem parte de faixas diferentes de preço (subtipos). Portanto, certos tipos de embalagens podem ser classificados como baratos, em conta ou caro (subtipos) a depender da média da faixa de preço.

Por exemplo: PETs que são caros possuem uma média em torno de 20 e PETs que são em conta possuem uma média em torno de 9.

- Para ficar mais organizado, podemos ordenar o tipo de embalagem por ordem alfabética ao utilizarmos o comando ORDER BY:

![image](https://user-images.githubusercontent.com/81119854/130633489-b83910e5-176a-40f6-9554-00766dc16ce1.png)

Assim, podemos visualizar a média de preços para produtos caro, barato e em conta para embalagens PET. 

- Podemos classificar o preço médio por sabor:

![image](https://user-images.githubusercontent.com/81119854/130634333-9bd6de94-0bf1-4192-97e4-7f38ec57ecf3.png)

Exercício: Veja o ano de nascimento dos clientes e classifique-os como: Nascidos antes de 1990 são velhos, nascidos entre 1990 e 1995 são jovens e nascidos depois de 1995 são crianças. Liste o nome do cliente e esta classificação.

![image](https://user-images.githubusercontent.com/81119854/130636252-fa09aafb-7b2b-47f2-8072-438543b1efa4.png)

# JOINS

- Vamos utilizar o comando JOIN para juntar duas tabelas com dados relacionados. Para tanto, devemos buscar tabelas que estejam relacionadas. Neste caso, escolhemos as tabelas de "notas_fiscais" e "tabela_de_vendedores" porque possuem o campo "MATRICULA" em comum.

![image](https://user-images.githubusercontent.com/81119854/131132141-abfc4f14-efe0-43a1-b02b-47ac22578ecb.png)

![image](https://user-images.githubusercontent.com/81119854/131132248-5e9f00d5-b907-4c6f-9e28-703138e9a89b.png)

- INNER JOIN: exibe tudo da tabela A e tudo da tabela B

![image](https://user-images.githubusercontent.com/81119854/131132954-d5f55cbb-e4c6-4e92-aa56-a057ae0e4276.png)

- Para sabermos a quantidade total de vendas por vendedor, podemos fazer:

![image](https://user-images.githubusercontent.com/81119854/131133971-0002a7c6-3a99-4840-9e92-43f311a15c7e.png)

- Podemos obter o mesmo resultado anterior ao aplicar um CROSS JOIN e depois atribuir a condição WHERE:

![image](https://user-images.githubusercontent.com/81119854/131134424-fe3bf861-5f86-43c3-9276-7535b954a698.png)

- Exercício: Obtenha o faturamento anual da empresa. Leve em consideração que o valor financeiro das vendas consiste em multiplicar a quantidade pelo preço.

![image](https://user-images.githubusercontent.com/81119854/131137433-5e25175c-b8f9-4271-9e28-892d8a0491e5.png)

- Para localizarmos um cliente que nunca comprou suco, podemos usar o LEFT JOIN para sabermos qual cliente está presenta na tabela de vendedores que não está presente na tabela de notas fiscais:

![image](https://user-images.githubusercontent.com/81119854/131158128-508724e9-dbde-4dec-ae97-6ee835bcb369.png)

Se quisermos fazer uma busca direcionada apenas para saber qual o cliente que não está presente na tabela de notas fiscais, fazemos:

![image](https://user-images.githubusercontent.com/81119854/131158522-f2a15f33-db03-4243-a897-19aca0a99968.png)

Poderíamos direcionar a busca para um determinado ano:

![image](https://user-images.githubusercontent.com/81119854/131158956-1cd51035-1f01-4546-a82b-fc6bfffac500.png)

Note que não há nenhum campo dentro das condições acima - porque no ano utilizado filtro todo mundo comprou.

- Não precisamos colocar prefixo ou sufixo com uma letra o tempo todo. Podemos utilizar um campo da tabela. Por exemplo, apenas os vendedores que o bairro está na tabela de clientes (ou clientes dos bairros que os vendedores tem escritório):

![image](https://user-images.githubusercontent.com/81119854/131161933-833387d3-f1b4-4e69-b6b3-d4c74078c247.png)

Ainda, nesta mesma forma, podemos selecionar campos específicos:

![image](https://user-images.githubusercontent.com/81119854/131163222-ec3662c4-e9a3-4312-91ae-b11efcd4ab72.png)

Também podemos especificar quais clientes estão de férias:

![image](https://user-images.githubusercontent.com/81119854/131163591-0dac3c69-bdb8-4d1b-94f0-79390f79791c.png)

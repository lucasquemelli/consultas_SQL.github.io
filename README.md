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

Projeto API Lol

Esse projeto visa extrair uma api com as versões de atualizações de campeões lançadas no League of Legends e seus status básicos.

Foram utilizado Python e suas bibliotecas Requests, Pandas e Psycopg2, PostgreSQL, Supebase versão free para hostear os dados(em outra versão eu abri as portas do roteador e funcionou a conexão externa ao PostgreSQL de outra máquina) e o dashboard foi feito no Tableau

Python

	No script primeiro eu recebo as versões através de uma API depois valido todos os links antes de extrair os dados, armazenando os que tiveram response 200 em uma váriavel e depois utilizar essa váriavel para extrair os dados.
	
	Os dados são extraídos em uma lista com diversos dicionários dentro e depois convertido em um DataFramme
	
	Eu conecto o python em um banco de dados local no PostgreSQL, crio uma tabela caso não exista, deleto todos os dados existentes na tabela e insiro os novos dados na mesma após armazenar todos os dados em uma lista.
	
O PostgreSQL 

	Eu uso apenas para armazenar os dados, como Tableau Public não permite eu conectar diretamente ao PostgreSQL.
	
Supabase

	Eu utilizei o prompt para conectar ao PostgreSQL e extrair a base em .csv pelo comando:
		COPY tabelacampeao TO 'E:\Jupyter\Projeto_API_LOL\tabelacampeao.csv' DELIMITER ',' CSV HEADER;
	Hospedei em um arquivo no Supabase, tambémm não é permitido linkar com o Tableau Public, então extraí um csv para importar no Tableu(Mantive essa etapa apenas para fins de aprendizagem que é o foco do projeto todo)
	
Tableau

	

	
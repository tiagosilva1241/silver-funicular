DOCUMENTAÇÃO RELATIVA À MINHA BASE DE DADOS PESSOAL DE RESTAURANTES EM LISBOA

0.DESCRIÇÃO GERAL DA BASE DE DADOS
Esta base de dados é constituída por 5 tabelas, em que a principal tem uma lista de restaurantes em Lisboa com dados como o contacto, a morada e a possibiliade de fazer reservas.
Noutras tabelas encontramos os aniversários dos meus amigos, as vezes que fui aos restaurantes, os pratos que têm e os funcionários.


1. INSTALAÇÃO DA BASE DE DADOS

1.1.
Fazer o download do xampp (https://www.apachefriends.org/download.html)

1.2.
Abrir o XAMPP, fazer start em MySQL, e clicar em Admin;

1.3.
Criar uma base de dados e dar-lhe o nome comidinhas_gostosas;

1.4.
Importar os dados e a estrutura da base de dados, através dos ficheiros respetivos (comidinhas_gostosas_estrutura.sql
e comidinhas_gostosas_dados.sql)



2. BACKUP DA BASE DE DADOS
2.1.
Na janela de controlador do XAMPP, clicar em Shell;

2.2.
Através do Shell, usar o comando "mysqldump -u root comidinhas_gostosas"
2.2.1.
Para fazer o back apenas dos dados: "mysqldump --no-create-info -u root comidinhas_gostosas > (NOME DO FICHEIRO)"
Para fazer o backup apenas da estrutura: "mysqldump --no-data -u root comidinhas_gostosas > (NOME DO FICHEIRO)"

3. RESTAURO DA BASE DE DADOS
3.1. Se a base de dados a restaurar não existir então criar com o comando:
mysql -u root  ”CREATE DATABASE destination_db”
Importar o ficheiro de dump no formato .sql:
mysql -u root < comidinhas_gostosas.sql

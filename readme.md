<h1> [Teste Estágio] Finalizado </h1>


*Considerações inciais

- tilizado no projeto php 7, Laravel, composer (para criação do projeto laravel), MySql.

*Configurando o banco de dados.

1 - Crie seu banco de dados.(Caso não aja banco para consultar, criar e organizar suas tabelas)

2 - Procure o arquivo .env na raiz do projeto e preencha os campos de acordo com as suas configurações:

- DB_CONNECTION=mysql (caso esteja usando mysql)

- DB_HOST=localhost (Host do seu banco)

- DB_PORT=3306 (Porta do banco)

- DB_DATABASE=Eduxe (Nome do banco)

- DB_USERNAME=root (Usuario do banco)

- DB_PASSWORD=pass (senha para acessar o banco)

    - obs.: dados preechidos são relativos ao meu ambiente de trabalho.

3 - Procure o arquivo /config/database.php. Dentro do return, procure 'connections' e vá na array 'mysqly' (ou SGBD utilizado), e preencha os campos de acordo com suas configurações anteriores:

- 'host' => env('DB_HOST', 'localhost'), (Host do seu banco)

- 'port' => env('DB_PORT', '3306'), (Porta do banco)

- 'database' => env('DB_DATABASE', 'Eduxe'), (Nome do banco)

- 'username' => env('DB_USERNAME', 'root'), (Usuario do banco)

- 'password' => env('DB_PASSWORD', 'pass'), (senha para acessar o banco)


4 - Abra o prompt de comando, vá até o diretorio do projeto, e por fim digite o codigo "php artisan migrate". Este codigo irá adicionar as tabelas necessarias para o uso do site.


5 - Continuando no diretorio do projeto no prompt de comando digite o codigo "php artisan db:seed". Este codigo irá adicionar duas linhas de dados na tabela para ser utilizado como preencimento previo e exemplificações na aplicação.


6 - Por fim utilize o comando "php artisan serve" para hospedar o site no seu localhost e acessa-lo no navegador com o o url dado pelo Laravel.


*Informações sobre o o desenvolvimento

- Ultilizando metodo MVC, facilitando o manejo e padronização das views, com blade. Views ecnontram-se em /resources/views

- Rotas especificadas em /routes/web.php

- Model encontra-se em /app

- Funções Get e Post encontram-se no controller app\Http\Controllers\candidatosController.php

- Na configuração do banco usamos dois arquivos que descrevem as tabelas, que no caso um é o migrate database\migrations\2019_10_30_074218_create_table_candidatos.php e o segundo é o seeder database\seeds\DatabaseSeeder.php. Onde o migrate cria as colunas e dita suas caracteriscas e o seeder é utilizado para alimentar automaticamente as primeiras linhas.

    - obs.: caso não utilize o seeder no inicio, entre na aplicação e e crie um novo candidato o seeder não funcionará pois o id especificado para os candidatos no arquivo DatabaseSeeder.php ja estarão preenchidos.

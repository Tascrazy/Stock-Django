1. Visão Geral do Projeto
O objetivo deste projeto foi construir uma aplicação web de gerenciamento de estoque de produtos utilizando o framework Django para o backend e React para o frontend. A aplicação oferece funcionalidades de CRUD (Criar, Ler, Atualizar e Excluir) para gerenciar os produtos no estoque.

Tecnologias utilizadas:

Backend: Django + Django REST Framework
Frontend: React + Tailwind CSS
Banco de Dados: SQLite (utilizado para desenvolvimento e testes)
Axios (para comunicação entre o frontend e o backend)
2. Estrutura do Backend (Django)
O backend foi desenvolvido utilizando o Django, com o Django REST Framework para criar as APIs RESTful. As principais funcionalidades implementadas incluem a criação, leitura, atualização e exclusão de produtos.

2.1. Modelos (Models)
O modelo Product foi criado para representar os produtos no banco de dados. Ele possui os seguintes campos:

name: nome do produto.
description: descrição do produto.
qty_stock: quantidade em estoque.
price: preço do produto.
added_date: data de adição do produto ao estoque.
2.2. Serializers
O ProductSerializer foi criado para converter os dados dos modelos em formato JSON e vice-versa. Este serializer foi utilizado para lidar com as operações de GET, POST, PUT e DELETE.

2.3. Views (Views)
A aplicação oferece três endpoints principais:

GET /api/products: retorna a lista de todos os produtos ou filtra por nome.
POST /api/products: cria um novo produto no estoque.
PUT /api/products/{id}: atualiza os dados de um produto existente.
DELETE /api/products/{id}: exclui um produto do estoque.
2.4. URLs (URLs)
As URLs foram configuradas no arquivo urls.py, utilizando expressões regulares para garantir que as requisições fossem direcionadas corretamente para as views adequadas.

2.5. Testes Backend
Testes básicos foram realizados utilizando o Postman para garantir que os endpoints estavam funcionando corretamente, realizando operações CRUD e retornando os resultados esperados.

3. Estrutura do Frontend (React)
O frontend foi desenvolvido utilizando React, com a estilização sendo feita via Tailwind CSS para garantir um design limpo e responsivo. A comunicação com o backend é feita através do Axios.

3.1. Componentes
ProductList: Exibe a lista de produtos cadastrados, com a possibilidade de excluir um produto.
ProductItem: Exibe as informações de um único produto e inclui os botões de editar e excluir.
ProductForm: Formulário utilizado para adicionar ou editar produtos. Inclui campos para nome, descrição, quantidade, preço e data de adição.
3.2. Funcionalidades
Listagem de Produtos: Ao acessar a aplicação, a lista de produtos é carregada automaticamente e exibida.
Adicionar Produto: O formulário de cadastro de produtos permite adicionar novos itens ao estoque.
Editar Produto: Ao clicar no botão "Editar", um formulário preenchido com os dados do produto é exibido para que o usuário possa alterar as informações.
Excluir Produto: Cada item na lista de produtos tem um botão "Excluir", que remove o produto do estoque.
Atualização Automática da Página: Após a adição ou remoção de um produto, a página é automaticamente atualizada para refletir as mudanças sem que o usuário precise recarregar a página manualmente.

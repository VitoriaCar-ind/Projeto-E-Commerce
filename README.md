# Esquema do Banco de Dados para E-commerce
![E-commerce](https://github.com/user-attachments/assets/b55c1f03-1374-4a45-b9da-50bbbfdf84c0)
Este repositório contém o diagrama do banco de dados desenvolvido para um sistema de e-commerce. O modelo está estruturado para gerenciar dados de clientes, produtos, pedidos, pagamentos, fornecedores e controle de estoque. Abaixo, uma descrição detalhada de cada tabela e seus relacionamentos:

Tabelas Principais
Fornecedor: Armazena as informações sobre os fornecedores que fornecem produtos ao sistema. Os campos incluem idFornecedor, RazaoSocial e CNPJ.

Produto: Contém detalhes dos produtos disponíveis no sistema. Inclui informações como idProduto, Categoria, Descrição e Valor.

Estoque: Armazena o local e a quantidade dos produtos no estoque. Os campos incluem idEstoque e Local.

Pedido: Registra os pedidos realizados pelos clientes, incluindo informações como idPedido, Status do Pedido, Descrição e Frete.

Pagamento: Armazena os métodos de pagamento associados a um pedido, com campos para Pix, Cartão e Boleto.

Cliente: Contém informações dos clientes, com distinção entre clientes Pessoa Jurídica (PJ) e Pessoa Física (PF). Inclui campos como idCliente, Nome, Identificação, e Endereço.

Tabelas de Relacionamento
Produto_has_Estoque: Relaciona os produtos com o estoque, permitindo especificar a quantidade de cada produto em diferentes locais de estoque.

Produtos_por_vendedor: Relaciona os fornecedores com os produtos que eles disponibilizam para venda, permitindo associar múltiplos fornecedores a um produto.

Status de entrega: Relaciona os pedidos e produtos com o status de entrega, permitindo acompanhar o progresso da entrega de cada produto de um pedido.

Relação do produto/Pedido: Relaciona os pedidos com os produtos solicitados, especificando a quantidade e permitindo associar um pedido a múltiplos produtos.

Cliente_Pedido: Associa os pedidos aos clientes que os realizaram, com uma distinção entre clientes PJ e PF, organizando os pedidos conforme o tipo de cliente.

Relacionamentos
Fornecedor ↔ Produto: A relação "Disponibilizando um produto" conecta fornecedores aos produtos que eles fornecem.
Produto ↔ Estoque: A tabela intermediária "Produto_has_Estoque" associa produtos ao estoque, registrando a quantidade de cada produto em cada local de estoque.
Pedido ↔ Cliente: O relacionamento de um pedido com um cliente é realizado pela tabela "Cliente_Pedido", permitindo identificar se o cliente é uma pessoa física (PF) ou jurídica (PJ).
Pedido ↔ Produto: A tabela "Relação do produto/Pedido" vincula os produtos com os pedidos, indicando a quantidade de cada produto no pedido e facilitando o controle de múltiplos produtos em um único pedido.
Pedido ↔ Pagamento: Relaciona pedidos aos métodos de pagamento, permitindo que cada pedido tenha um registro de pagamento específico.
Observações
O modelo de banco de dados foi desenvolvido para suportar um sistema de e-commerce básico, com controle de produtos, pedidos, clientes e fornecedores, além de métodos de pagamento. Este design também permite futuras expansões, como a inclusão de novos status de entrega ou métodos de pagamento.

Diagrama do Banco de Dados
O diagrama do banco de dados está disponível como uma imagem neste repositório para visualização da estrutura e dos relacionamentos entre as tabelas.


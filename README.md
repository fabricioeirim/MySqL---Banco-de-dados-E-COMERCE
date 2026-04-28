🧩 Diagrama Entidade-Relacionamento (ER)
O diagrama abaixo representa o modelo entidade‑relacionamento do banco de dados, evidenciando as entidades principais e seus relacionamentos.

  docs/images/diagrama_ecommerce.png


O modelo foi desenvolvido utilizando conceitos de normalização, relacionamentos 1:N e N:N, e integridade referencial.


🗄️ Modelo de Dados
🔹 Cliente (clients)
Armazena informações dos clientes da plataforma.

Nome completo
CPF (único)
Endereço

📌 Um cliente pode realizar vários pedidos.

🔹 Produto (product)
Contém o catálogo de produtos do e‑commerce.

Nome
Categoria
Avaliação
Indicação para público infantil
Tamanho (quando aplicável)


🔹 Pedido (orders)
Registra os pedidos realizados pelos clientes.

Status do pedido
Descrição
Valor do frete
Forma de pagamento

📌 Um pedido pertence a um cliente e pode conter vários produtos.

🔹 Produto / Pedido (productOrder)
Tabela de relacionamento N:N entre produtos e pedidos.

Quantidade do produto
Status de disponibilidade


🔹 Pagamento (payments)
Armazena informações de pagamento dos clientes.

Tipo de pagamento
Limite disponível


🔹 Estoque (productStorage e storageLocation)
Controla o armazenamento dos produtos.

Localização
Quantidade disponível


🔹 Fornecedor (supplier)
Cadastro de fornecedores.

Razão social
CNPJ (único)
Contato


🔹 Vendedor (seller)
Cadastro de vendedores terceiros (marketplace).

Razão social / nome fantasia
CNPJ ou CPF
Localização
Contato


🔹 Produto / Fornecedor (productSupplier)
Relacionamento entre produtos e fornecedores.

Quantidade fornecida


🔹 Produto / Vendedor (productSeller)
Relacionamento entre produtos e vendedores terceiros.

Quantidade disponível para venda


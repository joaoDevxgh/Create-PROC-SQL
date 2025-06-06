# 📚 Procedures para o Banco de Dados E-commerce

Este projeto apresenta a implementação de stored procedures para a manipulação eficiente de dados em um banco de dados de e-commerce. As operações de **inserção, atualização e remoção** são controladas por um parâmetro (`p_opcao`) dentro da procedure, otimizando a gestão via SQL.

## 🗂️ Tabelas Manipuladas

- `clients`
- `products`
- `orders`

## 🧠 Lógica de Controle

Cada procedure aceita um parâmetro `p_opcao`:
- 1 → Inserção
- 2 → Atualização
- 3 → Exclusão

## 💻 Exemplo de Execução

```sql
CALL sp_gerenciar_client(1, NULL, 'Carlos', 'A', 'Silva', '12345678901', 'Rua X, 123');
CALL sp_gerenciar_product(2, 1, 'Notebook Gamer', FALSE, 'eletronico', 4.8, 'G');
CALL sp_gerenciar_order(3, 5, NULL, NULL, NULL, NULL, NULL);

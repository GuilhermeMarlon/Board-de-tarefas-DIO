# Board Management System

## Descrição do Projeto

O **Board Management System** é uma aplicação Java que permite gerenciar boards (quadros), colunas e cards (tarefas). Ele foi projetado para ser uma ferramenta simples e eficiente para organizar tarefas em um fluxo de trabalho baseado em colunas, como o método Kanban.

A aplicação utiliza o banco de dados MySQL para persistência de dados e o Liquibase para gerenciar migrações de banco de dados. O sistema é executado em um terminal e oferece uma interface interativa para criar, visualizar, mover e gerenciar cards em diferentes colunas.

---

## Funcionalidades Principais

1. **Gerenciamento de Boards**:
   - Criar boards com colunas padrão (Inicial, Pendente, Final e Cancelado).
   - Adicionar colunas adicionais ao criar um board.
   - Excluir boards existentes.

2. **Gerenciamento de Cards**:
   - Criar cards associados a uma coluna inicial.
   - Mover cards entre colunas.
   - Bloquear e desbloquear cards com motivos específicos.
   - Cancelar cards movendo-os para a coluna de cancelamento.

3. **Visualização**:
   - Visualizar detalhes de um board, incluindo suas colunas e a quantidade de cards em cada uma.
   - Visualizar detalhes de uma coluna, incluindo os cards associados.
   - Visualizar detalhes de um card específico.

---

## Estrutura do Projeto

### Diretórios e Arquivos Importantes

- **`src/main/java/br/com/dio`**: Contém o código-fonte principal.
  - **`ui`**: Interface de usuário baseada em terminal.
  - **`service`**: Camada de serviços que implementa a lógica de negócios.
  - **`persistence`**: Camada de persistência que interage com o banco de dados.
  - **`dto`**: Objetos de transferência de dados.
  - **`exception`**: Exceções personalizadas.
- **`src/main/resources`**: Arquivos de configuração e migrações do Liquibase.
  - **`liquibase.properties`**: Configuração do Liquibase.
  - **`db/changelog`**: Scripts de migração do banco de dados.

---

## Diagrama de Funcionamento

```plaintext
+-------------------+       +-------------------+       +-------------------+
|                   |       |                   |       |                   |
|   Interface CLI   | ----> |   Camada Service  | ----> |   Banco de Dados  |
|                   |       |                   |       |                   |
+-------------------+       +-------------------+       +-------------------+
```


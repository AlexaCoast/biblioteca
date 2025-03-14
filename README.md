# Sistema de Empréstimos de Livros

## Sobre o Projeto
Este é um sistema para gerenciamento de empréstimos de livros em uma biblioteca.
O projeto permite o cadastro de usuários, livros, autores, editoras e categorias,
além do controle de empréstimos e devoluções.

### Objetivo
Criar um banco de dados para armazenar informações sobre livros, autores, usuários e empréstimos.

---
## Estrutura do Banco de Dados

### Tabelas

- **Usuários** (`id`, `nome`, `email`, `telefone`)
- **Livros** (`id`, `título`, `gênero`, `categoria`, `id_autor`, `id_editora`, `ano_publicacao`)
- **Autores** (`id`, `nome`, `nacionalidade`)
- **Editoras** (`id`, `nome`)
- **Empréstimos** (`id`, `id_livro`, `id_usuario`, `data_retirada`, `data_devolucao`)

### Relacionamentos

- **1:N entre Livros e Autores** - Um autor pode ter vários livros. A tabela `Livros` deve conter uma chave estrangeira (`id_autor`) referenciando a tabela `Autores`.
- **1:N entre Livros e Editoras** - Uma editora pode publicar vários livros. A tabela `Livros` deve conter uma chave estrangeira (`id_editora`) referenciando a tabela `Editoras`.
- **1:N entre Usuários e Empréstimos** - Um usuário pode ter vários empréstimos. A tabela `Empréstimos` deve conter uma chave estrangeira (`id_usuario`) referenciando a tabela `Usuários`.

---
## Tecnologias Utilizadas

- **Banco de Dados:** MySQL
- **Linguagem:** SQL para modelagem e consultas
- **Ferramentas:** MySQL Workbench 

---
## Funcionalidades

✅ Cadastro de usuários, livros, autores e editoras  
✅ Controle de empréstimos e devoluções  
✅ Consulta de disponibilidade de livros  
✅ Classificação de livros por categoria  
✅ Controle de datas de retirada e devolução  


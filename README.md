# Descrição da Funcionalidade do Sistema

Este projeto é uma **API para gerenciamento de filmes**, desenvolvida com ASP.NET Core, que permite realizar operações CRUD (Create, Read, Update e Delete) com validações robustas e o uso de **Data Transfer Objects (DTOs)** para lidar com as informações trafegadas entre cliente e servidor.

## Tecnologias Utilizadas:

- **ASP.NET Core**: Framework principal para desenvolvimento da API.
- **Entity Framework Core**: Mapeamento objeto-relacional (ORM) para interação com o banco de dados.
- **AutoMapper**: Mapeamento automático entre objetos (como entidades e DTOs).
- **MySQL**: Banco de dados relacional utilizado para persistência.
- **Swagger**: Documentação interativa da API.

## Estrutura do Projeto:

### Modelos:
- **Filme**: Representa a entidade do filme no banco de dados.

### DTOs:
- **CreateFilmeDto**: Define os dados necessários para adicionar um novo filme.
- **ReadFilmeDto**: Define os dados retornados ao consultar um filme.
- **UpdateFilmeDto**: Define os dados permitidos para atualizar um filme.

### Controller:
- **FilmeController**: Gerencia as requisições e responde com os dados solicitados ou status apropriado.

### Banco de Dados:
- Configurado com o **DbContext** `FilmeContext` para acesso e manipulação de filmes.

### Mapper:
- Configurações de mapeamento entre DTOs e modelos realizadas no perfil **FilmeProfile**.

## Configuração do Ambiente:

### Banco de Dados:
- Defina a string de conexão no **appsettings.json** em `FilmeConnection` com os detalhes do MySQL.

### Inicialização:
- Certifique-se de restaurar as dependências e executar as migrações do banco antes de iniciar a API:
  ```bash
  dotnet ef database update

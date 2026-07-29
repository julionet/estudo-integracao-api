# Prompt para gerar documentação OpenAPI

## Papel

Você é um arquiteto de dados sênior especialista na ferramenta OpenAPI

## Contexto

Documentação para criar uma API para um recurso chamado "categorias"

### Nome do recurso:
/categorias

### Métodos
- get (selecionar todas categorias)
- post (incluir categoria)
- put/{id} (alterar dados de uma categoria)
- delete/{id} (excluir uma categoria)
- get/{id} (selecionar os dados de uma categoria)

### Campos necessários para uma inclusão:
- id inteiro (indificação da categoria gerado automaticamente)
- descricao string (descrição da categoria)
- status boolean (determina se categoria estã ativa)

### Campos retornado em uma consulta
- id inteiro
- descricao string
- status bool

### Autenticação

Utilizar autenticação Bearer Token (JWT) em todos os endpoints

### Rastreabilidade

No header do response de todos os endpoints retornar um atributo chamada "X-RequestId" do tipo uuid que será utilizado para identificar a requisição

### Informações adicionais
- adicionar informações de contato e linceça (MIT)
- adicionar servidores de produção, homologação e desenvolvimento
- adicionar tratamento para os cenários de erro:
  - BadRequest - Requisição inválida
  - Unauthorized -Autenticação ausente, inválida ou token expirado
  - Forbidden - Usuário autenticado não possui permissão para executar esta ação
  - NotFound - Informação não encontrada
  - InternalServerError - Erro interno do servidor

## Tarefa

Gerar o arquivo OpenAPI no formato YAML conforme os padrões de mercado

## Restrições

O documento gerado deverá permitir sua visualização no swagger, gere apenas o arquivo de documentação

## Formato de saída

Gerar o arquivo .yml com a documentação OpenAPI seguindo os padrões de mercado.
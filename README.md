# Implementação básica GrpahQL em Go
- iniciar servidor GraphQL (GraphQL Playground em http://localhost:8080)
```bash
go run server.go
```
## Ferramentas e comandos uteis no desenvolvimento
**gqlgen**
- biblioteca em Go para criação de servers GraphQL
- instalar versão especifica do gqlgen
```bash
go get -d github.com/99designs/gqlgen@v0.14.0
```
- criar esqueleto de um novo projeto
- *Se você criar a pasta graphql e dentro o arquivo schema.graphqls com suas definições, o comando init cria todo o esqueleto a partir do seu schema. 
```bash
go run github.com/99designs/gqlgen init
```
- gerando resolvers 
```bash
go run github.com/99designs/gqlgen generate
```

## Considerações importantes
- Dependendo da utilização dos resolvers do GraphQL pode-se gerar "problemas" de consultas N+1.
- Para otimização de consultas N+1 existe uma possivel solução em https://gqlgen.com/reference/dataloaders/
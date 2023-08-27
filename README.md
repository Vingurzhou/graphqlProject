# graphqlProject

基于gqlgen的graphql服务

## 目录

### 初始化

```shell
gqlgen init
```

```
├── go.mod
├── go.sum
├── gqlgen.yml               - The gqlgen config file, knobs for controlling the generated code.
├── graph
│   ├── generated            - A package that only contains the generated runtime
│   │   └── generated.go
│   ├── model                - A package for all your graph models, generated or otherwise
│   │   └── models_gen.go
│   ├── resolver.go          - The root graph resolver type. This file wont get regenerated
│   ├── schema.graphqls      - Some schema. You can split the schema into as many graphql files as you like
│   └── schema.resolvers.go  - the resolver implementation for schema.graphql
└── server.go                - The entry point to your app. Customize it however you see fit
```

## 安装开发工具

```shell
go mod tidy
```

## 生成代码

```shell
go generate ./...
```

## 启动服务

```shell
go run server.go
```
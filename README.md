# Android Architecture MVVM

Esse repositório foi criado com o objetivo de instruir boas práticas para o desenvolvimento Android visando um código mais legível. Ele é utilizado **internamente** pela equipe de desenvolvimento de APPs da [Crosoften Tecnologia e Inovação](https://crosoften.com/) com o propositório de padronizar, estruturar e manter uma melhor qualidade de código.

## Arquitetura do projeto

Durante nossos projetos utilizamos o conceito de [Model-View-ViewModel (ou MVVM)](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93viewmodel), com algumas pequenas modificações para melhor se adequar ao nosso ambiente.

```java
br.com.crosoften.project
├─ commom
├─ data
   ├─ dao
   ├─ database
   └─ entities
├─ di
   ├─ base
   ├─ component
   └─ module
├─ network
   ├─ model
   └─ services   
├─ services
├─ utils
├─ view
   ├─ activities
   ├─ adapters
   ├─ animations
   ├─ custom
   ├─ dialogs
   └─ fragments
└─ viewmodel
```

`commom`: Camada referente a classes comums ao projeto, classes de domínio geral.

`data`: É a camada responsavel por acessar o banco de dados. Dentro dela temos: <br/>
`dao`: Camada de interfaces contendo os métodos de manipulação das entidades no banco.<br/>
`database`: Camada de configuração do banco de dados. <br/>
`entities`: Camada de entidades criadas no banco. <br/>

`di`: Camada responsável pelo controle de Injeção de Dependências. Dentro dela temos: <br/>
`base`: Camada de classes Bases que serão injetadas.<br/>
`component`: Camada de classes Components que irão prover métodos injetáveis. <br/>
`module`: Módulo que fornece todas as dependências necessárias. <br/>

`network`: Camada referente a parte de conexão com Api's Externas. Dentro dela temos: <br/>
`model`: Os modelos são POJOs (Plain Old Java Object) utilizados como comunicadores com WebService. <br/>
`services`: Camada de Interfaces que fornecem métodos comunicáveis com os webservices e injetados nas respectivas camadas de viewModel. <br/>

`services`: Camada de Interfaces a serem utilizadas durante a aplicação.

`utils`: Classes que não pertencem a nenhum grupo anterior, classes váriadas, podem ser guardadas no pacote útils. Por exemplo, uma classe para formatar datas (DataUtils).

`view`: Responsável por guardar as activities, fragments, adapters, animations, customs, dialogs, fragments, notifications, dentre outros . Basicamente, tudo relacionado a View do aplicativo.

`viewmodel`: Camada responsável pela parte lógica e a conexão entre a camada de view e a camada model.


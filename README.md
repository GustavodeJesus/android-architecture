# Android Architecture MVVM
trim_trailing_whitespace = false

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

`commom`: Pacote referente a classes comums ao projeto, classes de domínio geral.

`data`: É a camada responsavel por acessar o banco de dados. Dentro dela temos: 
      `dao`: Camada de interfaces contendo os métodos de manipulação das entidades no banco. <br />
      `database`: Camada de configuração do banco de dados. <br />
      `entities`: Camada de entidades criadas no banco. <br />
      
`ui`: Responsável por guardar as activities, fragments, adapters, notifications, action bar. Basicamente, tudo relacionado a View do aplicativo.

`presenters`: Responsável por vincular os models, providers e a ui; similar ao Controller do MVC.

`utils`: Classes que não pertencem a nenhum grupo anterior, classes váriadas, podem ser guardadas no pacote útils. Por exemplo, uma classe para formatar datas (DataUtils).

`models`: Os modelos são POJOs (Plain Old Java Object) que são populados a partir do banco de dados ou de uma resposta de algum WebService.


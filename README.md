# Android Architecture MVVM

Esse repositório foi criado com o objetivo de instruir boas práticas para o desenvolvimento Android visando um código mais legível. Ele é utilizado **internamente** pela equipe de desenvolvimento de APPs da [Crosoften Tecnologia e Inovação](https://crosoften.com/) com o propositório de padronizar, estruturar e manter uma melhor qualidade de código.

## Arquitetura do projeto

Durante nossos projetos utilizamos o conceito de [Model-View-ViewModel (ou MVVM)](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93viewmodel), com algumas pequenas modificações para melhor se adequar ao nosso ambiente.

```kotlin
br.com.crosoften.project
├─ commom
└─ data
   └─ adapters
├─ presenters
├─ utils
└─ ui
   ├─ adapters
   ├─ activities
   └─ fragments
```

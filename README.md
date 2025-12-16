# 📚 BooksJPA - API de Gerenciamento de Livros

> Uma API RESTful eficiente para catalogação e controle de acervo bibliográfico, utilizando a robustez do Spring Data JPA.

![Java](https://img.shields.io/badge/Java-17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.0-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![JPA](https://img.shields.io/badge/Spring_Data-JPA-gray?style=for-the-badge&logo=spring&logoColor=white)
![H2 Database](https://img.shields.io/badge/Database-H2-blue?style=for-the-badge&logo=h2&logoColor=white)

## 📖 Sobre o Projeto

O **BooksJPA** é um sistema backend desenvolvido para demonstrar a implementação de operações CRUD (Create, Read, Update, Delete) seguindo os padrões REST.

O foco principal do projeto é a utilização do **Spring Data JPA** para abstrair a complexidade das consultas SQL, permitindo manipulação de dados de forma orientada a objetos, com persistência ágil em banco de dados em memória (H2) para fins de desenvolvimento e testes rápidos.

## 🚀 Tecnologias Utilizadas

* **Spring Boot:** Framework core para inicialização rápida e configuração automática.
* **Spring Data JPA:** Camada de persistência para integração facilitada com bancos de dados.
* **H2 Database:** Banco de dados em memória (In-Memory), ideal para prototipagem sem necessidade de instalações complexas.
* **Maven:** Gerenciador de dependências e automação de build.
* **Lombok (Opcional):** Para redução de código boilerplate (Getters/Setters).

## 🔌 Endpoints da API

A aplicação disponibiliza os seguintes endpoints para consumo:

| Método | Rota | Descrição |
| :--- | :--- | :--- |
| `GET` | `/livros` | Lista todos os livros cadastrados |
| `GET` | `/livros/{isbn}` | Busca detalhes de um livro específico pelo ISBN |
| `POST` | `/livros` | Cadastra um novo livro no acervo |
| `PUT` | `/livros/{isbn}` | Atualiza os dados de um livro existente |
| `DELETE` | `/livros/{isbn}` | Remove um livro do sistema |

### 📝 Exemplo de JSON (Payload)

Para as requisições de `POST` (Criação) e `PUT` (Atualização), utilize o seguinte formato:

```json
{
  "titulo": "Arquitetura Limpa",
  "autor": "Robert C. Martin",
  "isbn": 123456789,
  "genero": "Tecnologia",
  "preco": 89.90
}

```

## 🔧 Como Executar
### Pré-requisitos
* Java JDK 17 ou superior.
* Maven instalado.

### Passo a Passo
1. **Clone o repositório:**
```bash
git clone [https://github.com/seu-usuario/books-jpa.git](https://github.com/seu-usuario/books-jpa.git)

```


2. **Acesse a pasta do projeto:**
```bash
cd books-jpa

```


3. **Execute a aplicação:**
```bash
mvn spring-boot:run

```



💾 Acessando o Banco H2
Como o projeto utiliza o banco H2 em memória, você pode visualizar os dados diretamente no navegador enquanto a aplicação estiver rodando.

1. Acesse: `http://localhost:8080/h2-console`
2. **JDBC URL:** `jdbc:h2:mem:testdb` (ou verifique seu `application.properties`)
3. **User:** `sa`
4. **Password:** (deixe em branco)

---

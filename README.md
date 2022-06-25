<h1 align="center">
    ELK Stack -Análise de Dados Governamentais
</h1>

<h3 align="center">
  Projeto de BD2 usando as ferramentas da elastic para visualização e manipulação de dados do portal de transparência.
</h3>

<p align="center">
  <a href="#-tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-projeto">Projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-instalação">Instalação</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-queries">Queries</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-como-contribuir">Como contribuir</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
</p>

<br>

## :rocket: Tecnologias e Ferramentas Utilizadas

Esse projeto foi desenvolvido com as seguintes tecnologias:

- [Elasticsearch](https://www.elastic.co/pt/what-is/elasticsearch)
- [Kibana](https://www.elastic.co/pt/kibana/)
- [Logstash](https://www.elastic.co/pt/logstash/)

## 💻 Projeto

Projeto de BD2 usando as ferramentas da elastic para visualização e manipulação de dados do portal de transparência.

<a href="https://github.com/danielVFS/elk-stack-visualizacao-de-dados-governamentais/trabalho-escrito" target="_blank" >Acesse o trabalho escrito no seguinte repositório.</a>

<br>

## 💻 Instalação

Para iniciar o **Projeto** faça o seguinte:

Faça o upload de sua base de dados em csv para a pasta /logstash/csv.

Em /pipeline/logstash.conf, altere:

```bash
path -> altere a partir de, com seu nome do arquivo no pasta csv /home/logstash/csv/insira-aqui-seu-csv.
filter -> altere o separator e columns, e mutate caso necessário.
output -> Altere user e password, após isso altere o index, essa será o index dentro do elasticsearch.
```

Com o arquivo logstash configurando, suba o docker-compose.

```bash
sudo docker-compose up -d
```

Assim que o projeto subir, acesse `localhost:5601`, você acessará a interface do Kibana.

Procure por data-managment em `http://localhost:5601/app/management/kibana/dataViews` e cria sua visualização de dados a partir de seu índice criado(o Kibana irá identificar seu índice).

Com isso, tudo estará pronto, você poderá acessar o `Console` para reproduzir as queries e `Dashboard` para visualização dos dados.

## 🔨 Queries

As queries para serem usadas no console, se encontrar em `logstash/querie-examples/queries.relatorio-folha-pagamento.txt`

## 🤔 Como contribuir

- Faça um fork desse repositório;
- Cria uma branch com a sua feature: `git checkout -b minha-feature`;
- Faça commit das suas alterações: `git commit -m 'feat: Minha nova feature'`;
- Faça push para a sua branch: `git push origin minha-feature`.

Depois que o merge da sua pull request for feito, você pode deletar a sua branch.

---

Feito por [Daniel Vitor](https://github.com/danielVFS) e [Rafael Souza](https://github.com/Rajael-dev)

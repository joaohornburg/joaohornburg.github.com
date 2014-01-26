---
layout: post
title: "Buscas rápidas com elasticsearch"
date: 2014-01-27 23:15:00 -0200
comments: true
published: false
categories:
- dev
- elasticsearch
- rails
---

Nesta retomada do blog, vou começar falando sobre elasticsearch. O post de hoje é o primeiro de uma [série][6] sobre o assunto. Hoje veremos para o que serve o elasticsearch, como funciona e como usá-lo em uma app _Ruby on Rails_.

[6]: ../../../../categories/elasticsearch/

## Por que elasticsearch? ##

Em muitos softwares há a necessidade de fazer pesquisas complexas. Pode ser uma busca aberta por atributos de um contato em um CRM, achar um post em um blog, um documento em um GED. Em todos esses casos, o que se quer é que a busca seja rápida e que ache conteúdo relevante.

É possível implementar esse tipo de busca com um banco relacional como o PostgreSQL, mas a busca será lenta e muito imprecisa para pesquisas textuais. Por exemplo: no [RD Station][1] utilizávamos uma gem chamada [scoped_search][2] que permite fazer buscas textuais em todos os campos de um contato que está na base. Funciona bem, mas faz tanto _join_ que só funciona para uma escala pequena.

Quando o número de acessos crescer, ou quando se estiver lidando com buscas em textos, a solução é utilizar um servidor de busca. E existem só dois maduros o suficiente: [Apache Solr][3] e [elasticsearch][4]. Ambos são baseados no [Lucene][5]. O Solr é mais antigo e por causa disso tem a vantagem de ser muito bem documentado e de ter uma comunidade grande. O elasticsearch possui uma API mais fácil de usar, é mais escalável e a sua comunidade está crescendo muito mais rápido do que a do Solr.

Por esses motivos decidi pelo _elastisearch_.

[1]: http://www.rdstation.com.br
[2]: https://github.com/wvanbergen/scoped_search
[3]: lucene.apache.org/solr
[4]: http://www.elasticsearch.org/
[5]: lucene.apache.org

## Como funciona ##

Quando dados são adicionados ao Lucene (engine de busca utilizada pelo elasticsearch e pelo Solr)

## Rails + elasticsearch

## Para saber mais ##

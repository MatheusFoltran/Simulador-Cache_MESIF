# Simulador de Operações com Memória e Cache (Protocolo MESIF)

Este projeto implementa um **simulador de operações de memória e cache** com **3 CPUs**, utilizando o protocolo **MESIF** para gerenciar a consistência da cache. O foco do simulador está na simulação do comportamento da cache, incluindo leitura e escrita de dados, bem como a gestão de suas consistências.

O sistema simula um **estoque de produtos**, onde cada produto tem informações como **preço**, **quantidade em estoque**, entre outros. As operações de leitura e escrita são simuladas para emular um ambiente de múltiplas CPUs interagindo com a memória e a cache de forma eficiente.

## Funcionalidades

- **Simulação de 3 CPUs**: Três unidades de processamento que competem pelo acesso à memória e cache.
- **Protocolo MESIF**: Implementação do protocolo MESIF para garantir a consistência da cache entre as CPUs.
  - **M** (Modified): O dado foi modificado e é válido apenas na cache.
  - **E** (Exclusive): O dado está único e não foi modificado.
  - **S** (Shared): O dado está em cache, mas pode ser modificado por outras CPUs.
  - **I** (Invalid): O dado não é válido.
  - **F** (Forward): O dado foi transmitido a outra cache.
- **Simulação de Sistema de Estoque**: Gestão de produtos com informações como **preço**, **quantidade em estoque**, **descrição** e **id do produto**.
- **Operações de Memória e Cache**: Leitura, escrita e consistência da cache entre as 3 CPUs.

## Arquitetura

O simulador é composto pelos seguintes elementos:

- **3 CPUs**: Cada CPU possui sua própria cache.
- **Memória Principal**: Armazena os dados dos produtos no estoque.
- **Cache**: Cada CPU possui uma cache que pode armazenar dados dos produtos. O protocolo MESIF garante a consistência entre as caches das CPUs.

## Autores:

- Matheus Foltran Consonni
- Thiago Henrique Calvi

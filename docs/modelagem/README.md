# Hub-Fiscal
Projeto profissioal


Sistema desenvolvido durante minha experiência profissional para automatizar e centralizar etapas do processo de recebimento, conferência e lançamento de notas fiscais no Sankhya.

## Sobre o projeto

O Hub Fiscal surgiu a partir de uma necessidade identificada no processo de lançamento de notas fiscais.

O processo manual exigia localizar as notas, conferir informações, digitar dados no ERP e, em alguns casos, repetir o lançamento para outra empresa. Além de consumir bastante tempo, esse fluxo aumentava a possibilidade de erros de digitação, lançamentos duplicados e divergências entre os registros.

A proposta do Hub Fiscal foi centralizar esse processo em uma única aplicação, permitindo receber as notas, validar suas informações, tratar pendências e realizar o lançamento diretamente no ambiente integrado ao Sankhya.

## Principais funcionalidades

* Captura automática de notas recebidas por e-mail.
* Importação de notas disponíveis no Portal de Compras do Sankhya.
* Upload manual de arquivos XML.
* Identificação de notas por chave de acesso para evitar duplicidade.
* Conferência de produtos antes do lançamento.
* Vinculação de produtos existentes ou cadastro de novos produtos.
* Processamento das informações financeiras presentes no XML.
* Lançamento das notas diretamente no Sankhya.
* Espelhamento dos lançamentos quando necessário.
* Acompanhamento do status dos lançamentos.
* Auditoria de divergências.
* Painel para acompanhamento das notas processadas.
* Registro de logs para acompanhamento das rotinas de processamento.

## Desenvolvimento

O projeto foi desenvolvido com apoio do Mitra, utilizando IA como ferramenta durante o processo de implementação.

O desenvolvimento envolveu a elaboração do escopo, definição dos requisitos, construção inicial da solução, integração com o ambiente Sankhya Analytics, análise das implementações geradas, realização de alterações e diversos ciclos de testes e correções.

A utilização de IA não substituiu a etapa de validação. As implementações precisaram ser analisadas, adaptadas e testadas de acordo com as necessidades do processo e com o comportamento esperado no ambiente da empresa.

## Integração com o Sankhya

O Hub Fiscal foi integrado ao ambiente Sankhya Analytics para permitir a comunicação entre a aplicação e o ERP utilizado pela empresa.

A integração fez parte do desenvolvimento da solução e exigiu configurações, ajustes e testes para que os processos de importação, lançamento e acompanhamento funcionassem de acordo com os requisitos definidos.

Por se tratar de um ambiente empresarial, os detalhes técnicos específicos da integração não são disponibilizados neste repositório.

## Processo

O fluxo principal da solução pode ser representado da seguinte forma:

```text
Recebimento da nota
        ↓
Captura ou importação do XML
        ↓
Validação da nota
        ↓
Verificação dos produtos
        ↓
Conferência das informações
        ↓
Processamento
        ↓
Integração com o Sankhya
        ↓
Lançamento
        ↓
Acompanhamento
        ↓
Auditoria
```

## Validações e regras de negócio

Durante o desenvolvimento foram implementadas regras para reduzir erros durante o processo, incluindo:

* validação da chave de acesso para evitar a captura de uma mesma nota mais de uma vez;
* bloqueio do lançamento quando existem produtos pendentes de identificação;
* controle do lançamento entre empresas;
* verificação de divergências entre lançamentos;
* validação das informações financeiras antes do envio;
* acompanhamento do status da nota após o lançamento;
* controle por data de corte para evitar o processamento indevido de documentos antigos.

## Testes

O desenvolvimento passou por diversos ciclos de testes, alterações e correções.

Foram validados cenários como:

* notas recebidas por diferentes origens;
* documentos duplicados;
* produtos não identificados;
* vinculação de produtos existentes;
* cadastro de novos produtos;
* notas com diferentes condições de pagamento;
* lançamentos entre empresas;
* divergências de valores;
* notas lançadas e posteriormente alteradas ou excluídas no ERP;
* comunicação entre o Hub Fiscal e o Sankhya.

## Minha participação

Minha atuação no projeto envolveu:

* identificação e análise do problema;
* levantamento das necessidades do processo;
* elaboração do escopo;
* definição dos requisitos da solução;
* desenvolvimento com apoio de IA;
* integração com o Sankhya Analytics;
* análise e alteração das implementações;
* realização de testes;
* identificação e correção de problemas;
* validação do funcionamento da solução.

## Tecnologias e ferramentas

* Mitra
* Sankhya Analytics
* Sankhya ERP
* OCR
* XML
* Integração de sistemas
* Automação de processos

## Confidencialidade

Este repositório apresenta o projeto como um case profissional, utilizando somente informações que podem ser divulgadas publicamente.

Não são disponibilizados:

* código-fonte proprietário;
* dados fiscais reais;
* dados de clientes ou fornecedores;
* CNPJ, CPF ou outras informações pessoais;
* credenciais ou chaves de acesso;
* informações financeiras reais;
* configurações internas;
* endpoints privados;
* informações de infraestrutura;
* dados ou documentos pertencentes à empresa.

Os exemplos apresentados neste repositório são genéricos ou fictícios e têm como objetivo apenas demonstrar o funcionamento e as características da solução.

## Objetivo do case

Este projeto registra uma experiência prática de desenvolvimento de uma solução para um problema real de negócio, envolvendo levantamento de requisitos, automação de processos, desenvolvimento assistido por IA, integração de sistemas, testes e validação em ambiente empresarial.


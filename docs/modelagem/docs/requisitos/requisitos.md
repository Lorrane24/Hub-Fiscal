# Requisitos — Hub Fiscal

## 1. Requisitos Funcionais

### RF01 — Monitoramento de documentos fiscais

O sistema deve monitorar as fontes definidas para recebimento de documentos fiscais e identificar novos documentos disponíveis para processamento.

### RF02 — Recebimento de documentos por e-mail

O sistema deve verificar periodicamente a caixa de e-mail configurada para identificar documentos fiscais recebidos.

### RF03 — Recebimento de documentos pelo Portal de Compras

O sistema deve consultar periodicamente a fila de documentos disponível no Portal de Compras do Sankhya.

### RF04 — Identificação da chave de acesso

O sistema deve identificar a chave de acesso da Nota Fiscal Eletrônica (NF-e) a partir dos dados disponíveis no documento fiscal.

### RF05 — Consulta e visualização dos documentos

O sistema deve disponibilizar os documentos identificados para consulta e acompanhamento do processamento.

### RF06 — Lançamento da nota fiscal no Sankhya

O sistema deve permitir o processamento e lançamento dos documentos fiscais selecionados no ambiente Sankhya, conforme as empresas configuradas.

### RF07 — Validação de produtos

O sistema deve verificar os produtos presentes no documento fiscal e identificar aqueles que não possuem correspondência no cadastro utilizado pelo Sankhya.

### RF08 — Tratamento de produtos não reconhecidos

O sistema deve permitir o tratamento dos produtos não reconhecidos, possibilitando seu registro ou substituição conforme a necessidade do processo.

### RF09 — Registro das parcelas

O sistema deve processar as informações de parcelas presentes no XML da NF-e, incluindo seus respectivos valores e vencimentos.

### RF10 — Prevenção de duplicidade

O sistema deve verificar a chave de acesso da NF-e antes do lançamento, evitando o processamento duplicado de uma mesma nota fiscal.

### RF11 — Processamento por empresa

O sistema deve direcionar o lançamento do documento fiscal para a empresa correspondente dentro do ambiente Sankhya.

### RF12 — Acompanhamento do processamento

O sistema deve apresentar o status dos documentos durante o processo de recebimento, validação e lançamento.

### RF13 — Consulta de documentos processados

O sistema deve permitir a consulta dos documentos que já foram processados, possibilitando o acompanhamento do histórico.

---

## 2. Requisitos Não Funcionais

### RNF01 — Disponibilidade

O sistema deve realizar as verificações periódicas das fontes configuradas de acordo com os intervalos definidos para cada origem.

### RNF02 — Integridade dos dados

O sistema deve preservar a integridade das informações obtidas dos documentos fiscais durante o processamento.

### RNF03 — Segurança

O sistema deve restringir o acesso às funcionalidades conforme as permissões configuradas para os usuários.

### RNF04 — Rastreabilidade

O sistema deve permitir identificar o documento processado e seu respectivo resultado, possibilitando o acompanhamento do processo.

### RNF05 — Confiabilidade

O sistema deve realizar validações antes do lançamento para reduzir a ocorrência de registros incorretos ou duplicados.

### RNF06 — Usabilidade

As informações de processamento devem ser apresentadas de forma organizada, permitindo que o usuário acompanhe as etapas e identifique pendências.

### RNF07 — Integração

O sistema deve ser capaz de trabalhar integrado ao ambiente Sankhya e às fontes de documentos fiscais definidas para o processo.

### RNF08 — Privacidade e proteção de dados

O sistema deve tratar os dados envolvidos no processo de acordo com os princípios aplicáveis da Lei Geral de Proteção de Dados (LGPD).

---

## 3. Priorização

Os requisitos podem ser classificados de acordo com sua importância para o funcionamento do processo:

| Prioridade | Requisitos                                                  |
| ---------- | ----------------------------------------------------------- |
| Alta       | RF01, RF03, RF04, RF06, RF07, RF10, RF11                    |
| Média      | RF05, RF08, RF09, RF12, RF13                                |
| Baixa      | Funcionalidades complementares de consulta e acompanhamento |

## 4. Observação

Os requisitos representam a visão funcional do Hub Fiscal e devem permanecer coerentes com o escopo definido para o projeto, com as regras de negócio, com a modelagem e com as funcionalidades efetivamente implementadas ou demonstradas.


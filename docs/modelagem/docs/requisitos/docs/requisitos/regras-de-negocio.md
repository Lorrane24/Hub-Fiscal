
# Regras de Negócio — Hub Fiscal

## RN01 — Unicidade da Nota Fiscal

Uma Nota Fiscal Eletrônica (NF-e) não deve ser lançada novamente quando sua chave de acesso já tiver sido processada pelo sistema.

## RN02 — Validação antes do lançamento

O documento fiscal deve passar pelas validações necessárias antes de ser encaminhado para lançamento no Sankhya.

## RN03 — Identificação do produto

Os produtos presentes no documento fiscal devem ser comparados com os produtos disponíveis no cadastro utilizado pelo processo.

## RN04 — Produto não identificado

Quando um produto presente na NF-e não for reconhecido, o processamento deve identificar a pendência para que seja realizado o tratamento necessário.

## RN05 — Tratamento de produto

Produtos não identificados podem ser cadastrados ou relacionados a um produto existente, conforme a necessidade do processo.

## RN06 — Empresas de destino

O lançamento deve ser realizado na empresa correspondente ao documento fiscal, considerando as empresas configuradas no processo.

## RN07 — Parcelas da nota fiscal

As informações de pagamento presentes no XML devem ser consideradas no processamento das parcelas da NF-e.

## RN08 — Dados das parcelas

Cada parcela deve manter as informações correspondentes ao seu valor e vencimento conforme os dados disponíveis no XML.

## RN09 — Origem dos documentos

O sistema deve considerar as diferentes fontes configuradas para recebimento dos documentos fiscais, incluindo e-mail e Portal de Compras.

## RN10 — Periodicidade de consulta

As fontes de documentos devem ser consultadas de acordo com a periodicidade definida para cada origem.

## RN11 — Status do processamento

O documento deve possuir uma situação que permita acompanhar sua evolução durante o processo de recebimento, validação e lançamento.

## RN12 — Tratamento de pendências

Documentos que apresentarem inconsistências durante o processamento devem permanecer identificados como pendentes até que a situação seja tratada.

## RN13 — Rastreabilidade

O processamento deve permitir relacionar o documento fiscal às informações utilizadas durante seu lançamento, possibilitando o acompanhamento do processo.

## RN14 — Integridade das informações

Os dados obtidos do documento fiscal devem ser preservados durante o processamento, evitando alterações indevidas nas informações utilizadas para o lançamento.

## RN15 — Controle de acesso

As funcionalidades do sistema devem estar disponíveis de acordo com as permissões definidas para cada usuário.

---

## Relação entre Requisitos e Regras de Negócio

| Requisito                        | Regras relacionadas |
| -------------------------------- | ------------------- |
| RF01 — Monitoramento             | RN09, RN10          |
| RF03 — Portal de Compras         | RN09, RN10          |
| RF04 — Chave de acesso           | RN01                |
| RF06 — Lançamento no Sankhya     | RN02, RN06          |
| RF07 — Validação de produtos     | RN03                |
| RF08 — Tratamento de produtos    | RN04, RN05          |
| RF09 — Registro das parcelas     | RN07, RN08          |
| RF10 — Prevenção de duplicidade  | RN01                |
| RF11 — Processamento por empresa | RN06                |
| RF12 — Acompanhamento            | RN11, RN12          |
| RF13 — Consulta de documentos    | RN11, RN13          |

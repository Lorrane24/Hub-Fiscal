# Fluxo do Processo — Hub Fiscal

## 1. Visão geral

O fluxo do Hub Fiscal representa as principais etapas realizadas desde a identificação de um novo documento fiscal até seu processamento e lançamento no ambiente Sankhya.

O processo envolve monitoramento das fontes de documentos, identificação da NF-e, validações, tratamento de pendências, processamento e acompanhamento do resultado.

## 2. Fluxo principal

1. O Hub Fiscal realiza o monitoramento das fontes configuradas.
2. Um novo documento fiscal é identificado.
3. O sistema obtém os dados disponíveis do documento.
4. A chave de acesso da NF-e é identificada.
5. O sistema verifica se a nota já foi processada.
6. Caso a nota já tenha sido processada, o documento é identificado como duplicado e não é processado novamente.
7. Caso a nota ainda não tenha sido processada, o sistema realiza as validações necessárias.
8. Os produtos presentes na nota são verificados.
9. Caso existam produtos não reconhecidos, a pendência é apresentada para tratamento.
10. Após o tratamento das pendências, o documento pode continuar o processamento.
11. O sistema identifica a empresa de destino.
12. As informações da nota são preparadas para o lançamento.
13. As informações das parcelas são consideradas no processamento.
14. O documento é processado no ambiente Sankhya.
15. O resultado do processamento é registrado.
16. O documento fica disponível para acompanhamento e consulta do histórico.

## 3. Fluxo de decisão

### Documento já processado

Se a chave de acesso da NF-e já estiver registrada como processada, o sistema deve impedir o processamento duplicado.

### Produto não identificado

Se algum produto da NF-e não for reconhecido, o documento deve permanecer com uma pendência até que o produto seja tratado.

### Documento apto para processamento

Quando as validações forem concluídas e não houver pendências impeditivas, o documento poderá seguir para processamento no Sankhya.

## 4. Fluxo simplificado

```text
Início
  ↓
Monitorar fontes
  ↓
Identificar documento
  ↓
Identificar chave de acesso
  ↓
Já foi processado?
  ├── Sim → Identificar duplicidade → Encerrar processamento
  │
  └── Não
        ↓
      Validar documento
        ↓
      Existem produtos não reconhecidos?
        ├── Sim → Tratar pendência
        │            ↓
        │       Continuar processamento
        │
        └── Não
             ↓
       Identificar empresa
             ↓
       Preparar informações
             ↓
       Processar no Sankhya
             ↓
       Registrar resultado
             ↓
       Disponibilizar para acompanhamento
             ↓
            Fim
```

## 5. Fontes de documentos

O Hub Fiscal considera as fontes configuradas para recebimento de documentos fiscais.

### E-mail

A caixa de e-mail configurada é monitorada periodicamente para identificação de novos documentos fiscais.

### Portal de Compras

A fila de documentos disponível no Portal de Compras do Sankhya é consultada periodicamente para identificação de novos documentos.

## 6. Resultado do processo

Ao final do processamento, o documento deve possuir uma situação que permita identificar seu resultado, como processamento concluído ou pendência para tratamento.

O fluxo deve permitir a rastreabilidade do documento desde sua identificação até o resultado do processamento.


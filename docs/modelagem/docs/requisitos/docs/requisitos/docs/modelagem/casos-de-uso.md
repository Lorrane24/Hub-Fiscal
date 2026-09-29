# Casos de Uso — Hub Fiscal

## 1. Atores

### Usuário do sistema

Responsável por acompanhar os documentos fiscais, verificar pendências e realizar os tratamentos necessários durante o processo.

### Hub Fiscal

Responsável pela execução automatizada das etapas de monitoramento, identificação, validação e processamento dos documentos fiscais.

### Sankhya

Sistema integrado ao Hub Fiscal para consulta, validação e lançamento das informações fiscais.

### Fonte de documentos fiscais

Origem dos documentos recebidos pelo Hub Fiscal, incluindo e-mail e Portal de Compras.

---

## 2. Casos de Uso

### UC01 — Monitorar documentos fiscais

**Ator principal:** Hub Fiscal

**Descrição:**
O sistema verifica periodicamente as fontes configuradas e identifica novos documentos fiscais disponíveis para processamento.

**Pré-condições:**

* As fontes de documentos devem estar configuradas.
* O sistema deve estar disponível para realizar a consulta.

**Fluxo principal:**

1. O Hub Fiscal inicia a consulta da fonte configurada.
2. O sistema verifica a existência de novos documentos.
3. Os documentos encontrados são identificados.
4. Os documentos são disponibilizados para processamento.

---

### UC02 — Consultar documento fiscal

**Ator principal:** Usuário do sistema

**Descrição:**
Permite ao usuário visualizar os documentos fiscais identificados pelo Hub Fiscal.

**Fluxo principal:**

1. O usuário acessa a área de documentos.
2. O sistema apresenta os documentos disponíveis.
3. O usuário seleciona um documento.
4. O sistema apresenta as informações disponíveis do documento.

---

### UC03 — Validar documento fiscal

**Ator principal:** Hub Fiscal

**Descrição:**
O sistema realiza as validações necessárias antes do lançamento do documento no Sankhya.

**Fluxo principal:**

1. O sistema identifica o documento.
2. Obtém os dados necessários para processamento.
3. Verifica a chave de acesso.
4. Verifica os produtos relacionados.
5. Verifica as informações necessárias para o lançamento.
6. Define o resultado da validação.

**Fluxo alternativo:**

* Caso seja identificada uma inconsistência, o documento é sinalizado como pendente para tratamento.

---

### UC04 — Verificar duplicidade

**Ator principal:** Hub Fiscal

**Descrição:**
Verifica se a chave de acesso da NF-e já foi processada para evitar lançamentos duplicados.

**Fluxo principal:**

1. O sistema identifica a chave de acesso.
2. Consulta os registros existentes.
3. Compara a chave identificada com os registros encontrados.
4. Caso não exista registro correspondente, o processamento continua.

**Fluxo alternativo:**

* Caso a chave já tenha sido processada, o sistema impede o processamento duplicado e identifica a ocorrência.

---

### UC05 — Tratar produto não identificado

**Ator principal:** Usuário do sistema

**Descrição:**
Permite tratar produtos presentes na NF-e que não foram reconhecidos durante a validação.

**Fluxo principal:**

1. O sistema identifica o produto não reconhecido.
2. O usuário visualiza a pendência.
3. O usuário realiza o tratamento necessário.
4. O sistema atualiza a situação do produto.
5. O documento pode continuar o processamento quando as pendências forem resolvidas.

---

### UC06 — Processar documento fiscal

**Ator principal:** Hub Fiscal

**Atores secundários:** Sankhya

**Descrição:**
Realiza o processamento do documento fiscal após as validações necessárias.

**Fluxo principal:**

1. O sistema verifica se o documento está apto para processamento.
2. O sistema identifica a empresa de destino.
3. O sistema prepara as informações necessárias.
4. O Hub Fiscal envia/processa as informações no Sankhya.
5. As informações das parcelas são consideradas no processamento.
6. O sistema registra o resultado do processamento.

---

### UC07 — Acompanhar processamento

**Ator principal:** Usuário do sistema

**Descrição:**
Permite acompanhar a situação dos documentos durante o processo.

**Fluxo principal:**

1. O usuário acessa a área de acompanhamento.
2. O sistema apresenta os documentos processados.
3. O usuário consulta a situação de cada documento.
4. O usuário identifica documentos concluídos ou pendentes.

---

### UC08 — Consultar histórico

**Ator principal:** Usuário do sistema

**Descrição:**
Permite consultar informações relacionadas aos documentos que já passaram pelo processamento.

**Fluxo principal:**

1. O usuário acessa o histórico.
2. O sistema apresenta os registros disponíveis.
3. O usuário seleciona um documento.
4. O sistema apresenta as informações relacionadas ao processamento.


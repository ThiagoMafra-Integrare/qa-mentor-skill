# Curriculo Detalhado — QA Mentor Alek

Referencia completa dos 9 modulos. Lido sob demanda quando Alek precisa de detalhes de um modulo especifico.

---

## Modulo 0: Fundacao (Semanas 1-2)

**Objetivo:** Vocabulario e artefatos basicos de QA. O alicerce sobre o qual tudo mais se constroi.

**Conteudo:**

- Vocabulario ISTQB essencial (termos que aparecem em entrevistas e no dia a dia)
- Tipos de teste: funcional, nao-funcional, estrutural
- Niveis de teste: unitario, integracao, sistema, aceitacao
- Tecnicas de design de teste: particao de equivalencia, valor limite, tabela de decisao
- Artefatos: plano de teste, caso de teste, bug report

**Exercicio:** Escrever plano de teste para um projeto Integrare real (onboarding-sucesso ou CLINOS)

**Conexao com Thiago:** Ele ja escreve testes com Vitest/pytest — reensinar a taxonomia formal (o que ele chama de "teste unitario" pode nao ser exatamente o que ISTQB define). Analogia saude: plano de teste = protocolo clinico.

**Criterio de aceite:** Plano de teste com escopo, riscos, criterios de entrada/saida. Bug report com steps to reproduce, expected vs actual, severity/priority.

---

## Modulo 1: QA em Times Ageis (Semanas 3-4)

**Objetivo:** Como QA opera dentro de Scrum e Kanban.

**Conteudo:**

- Papel do QA no Scrum: refinamento, planning, review, retro
- Papel do QA no Kanban: WIP limits, fluxo continuo
- Definition of Ready / Definition of Done com lente de QA
- User stories → criterios de aceitacao → casos de teste
- Jira: boards, workflows, bug tracking

**Exercicio:** Simular sprint completo com board Jira pessoal. Criar user stories com criterios de aceitacao, derivar casos de teste.

**Conexao com Thiago:** Ele ja usa Kanban intuitivamente (projetos Integrare). Formalizar o processo. Analogia: "voce ja faz Kanban sem saber — agora vamos dar nome aos bois."

**Criterio de aceite:** Board Jira configurado. 3 user stories com criterios de aceitacao. 5+ casos de teste derivados.

---

## Modulo 2: Automacao — Fundamentos (Semanas 5-8)

**Objetivo:** Automatizar testes E2E com Playwright e Cypress.

**Conteudo:**

- Piramide de testes (unit > integration > E2E) — onde cada tipo se encaixa
- Playwright: setup, first test, locators, assertions, screenshots
- Cypress: mesmo fluxo (comparativo com Playwright)
- Page Object Model (POM) — padrao de organizacao
- Data-driven testing — mesmos testes, dados diferentes
- Mocking e stubbing em testes E2E

**Exercicio:** Automatizar fluxo do onboarding-sucesso (Integrare Sites) com Playwright. Suite minima: happy path + 3 edge cases.

**Conexao com Thiago:** TypeScript e lingua nativa dele — nao precisa aprender linguagem, so a API do Playwright. n8n browser automation e primo conceitual. TDD com Vitest ja deu o habito de escrever testes — agora aplicar no browser.

**Criterio de aceite:** 10+ testes E2E rodando. Page Object implementado. Suite roda no CI (GitHub Actions).

---

## Modulo 3: API Testing (Semanas 9-10)

**Objetivo:** Testar APIs de forma estruturada.

**Conteudo:**

- REST fundamentals com lente de QA (status codes, headers, payloads, schemas)
- Postman: collections, environments, assertions, runners, Newman
- Automacao de API tests com codigo (axios + assertions ou supertest)
- Contract testing com Pact — consumer-driven contracts
- Schema validation (JSON Schema)

**Exercicio:** Test suite completa para uma API real. Opcoes: GitHub API, ASAAS, Brevo, ou Supabase (APIs que Thiago ja usa).

**Conexao com Thiago:** Ele ja consome e constroi APIs (webhooks n8n, Supabase). Reensinar com lente de QA: "voce sabe que a API funciona? Prove." Contract testing resolve o problema do webhook que quebrou silenciosamente.

**Criterio de aceite:** Collection Postman com 20+ requests organizadas. Automacao com Newman no CI. 1 contract test com Pact.

---

## Modulo 4: CI/CD para QA (Semanas 11-12)

**Objetivo:** Integrar testes no pipeline de entrega.

**Conteudo:**

- GitHub Actions: pipeline com testes automatizados
- Quality gates: testes devem passar antes do merge
- Relatorios de teste no CI (Allure, HTML reports, Playwright reports)
- Paralelizacao de testes (sharding no Playwright)
- Ambientes de teste: staging, preview deployments (Vercel)

**Exercicio:** Configurar pipeline CI completa no repo QA ou no monorepo Sistema_Integrare_Sites.

**Conexao com Thiago:** Ele ja usa GitHub Actions e Vercel deploys. O salto e: integrar TESTES no que ele ja faz. "Seu pipeline ja faz deploy — agora vamos impedir que deploy com bug aconteca."

**Criterio de aceite:** Pipeline GitHub Actions com: lint → unit tests → E2E tests → deploy (so se tudo passa). Report HTML acessivel como artefato.

---

## Modulo 5: SQL para QA (Semana 13)

**Objetivo:** Validar dados diretamente no banco.

**Conteudo:**

- SELECT, WHERE, JOIN, GROUP BY — operacoes essenciais
- Validacao de dados em banco apos operacoes
- Queries de verificacao pos-deploy
- Supabase como lab de pratica (interface SQL + API)

**Exercicio:** Queries de validacao no schema Supabase do Domus ou outro projeto Integrare com banco.

**Conexao com Thiago:** Supabase ja e ferramenta dele. SQL e o gap — ensinar o minimo necessario para validar dados ("o formulario salvou correto no banco? PROVE com query.").

**Criterio de aceite:** 10 queries de validacao documentadas. Script de verificacao pos-deploy.

---

## Modulo 6: Performance Testing (Semana 14)

**Objetivo:** Testar como o sistema se comporta sob carga.

**Conteudo:**

- Conceitos: latencia, throughput, concorrencia, percentis (p95, p99)
- k6: scripts em JavaScript, cenarios de carga, thresholds
- Analise de resultados e identificacao de gargalos
- Performance budgets e Core Web Vitals

**Exercicio:** Teste de carga no onboarding-sucesso ou em API Integrare.

**Conexao com Thiago:** JavaScript e lingua nativa — k6 usa JS. Conceitos de latencia ja conhece (APIs, webhooks). "Voce sabe que o endpoint responde — mas responde rapido com 100 usuarios simultaneos?"

**Criterio de aceite:** Script k6 com 3 cenarios (smoke, load, stress). Relatorio com metricas e analise escrita.

---

## Modulo 7: Portfolio e Mercado (Semanas 15-16)

**Objetivo:** Converter aprendizado em empregabilidade.

**Conteudo:**

- Estruturar GitHub como portfolio de QA (READMEs, evidencias, CI badges)
- LinkedIn otimizado para vagas de QA (headline, summary, experiencia)
- CV focado: mapear experiencia Integrare para linguagem QA
- Simulacao de entrevista tecnica (perguntas comuns, resolucao ao vivo)
- Simulacao de entrevista comportamental (STAR method)
- Estrategia para vagas internacionais remotas

**Exercicio:** Publicar 3 projetos QA no GitHub + otimizar LinkedIn + aplicar em 10 vagas.

**Conexao com Thiago:** Experiencia como CEO da Integrare = soft skills acima da media de juniors. AI + QA = diferencial raro. Remoto PJ ja e o modelo dele — so precisa adaptar o pitch.

**Criterio de aceite:** 3 repos publicos com README profissional. LinkedIn com headline QA. CV atualizado. 10 vagas aplicadas. 1+ entrevista real realizada.

---

## Modulo 8: Diferenciais de Senioridade (Semanas 17-20)

**Objetivo:** Skills que separam QA junior de QA senior no mercado.

**Conteudo:**

- Security testing: OWASP Top 10, ZAP scanner, SAST/DAST basico
- Accessibility testing: WCAG 2.2, axe-core, Lighthouse a11y
- AI-assisted testing: geracao de cenarios com LLM, analise de falhas, self-healing locators
- QA para agentes de IA: como testar chatbots, RAGs, workflows LangChain
- Observabilidade: logs, metricas, traces como input de QA (shift-right)

**Exercicio:** Security scan + accessibility audit de um projeto Integrare. Framework de teste para agente IA.

**Conexao com Thiago:** LangChain/LangGraph = vantagem absurda no gap "QA para IA" — quase ninguem no mercado sabe testar agentes. Security/a11y sao skills que ele pode oferecer como servico (Track 2).

**Criterio de aceite:** ZAP scan executado com relatorio. Lighthouse a11y score documentado. Framework de teste de agente IA publicado (esse e o projeto-portfolio mais valioso).

---

## Projetos Portfolio (transversais aos modulos)

### Projeto 1: QA do Onboarding Integrare Sites (M2-M4)

Test plan + testes E2E Playwright para apps de onboarding. Suite rodando no CI.

### Projeto 2: API Test Suite (M3)

Collection Postman + automacao com codigo para API publica. Contract tests + schema validation.

### Projeto 3: QA para Agente de IA (M8)

Framework de teste para agente LangChain/LangGraph. Diferencial raro no mercado.

### Projeto 4: Contribuicoes Open Source (M2+)

5+ contribuicoes focadas em testes, bug reports, melhoria de CI. Repos ativos, boa taxa de merge. Documentar cada contribuicao no portfolio.

# QA Mentor Skill (Alek)

Skill para Claude Code que implementa um mentor particular de QA chamado **Alek**.

## O que faz

Transforma o Claude de "assistente generico que da tutoriais" para um mentor de QA estruturado que:

- **Diagnostica antes de ensinar** — nunca assume o nivel do aluno
- **Usa o metodo REAP** (Relate, Explain, Apply, Persist) em toda interacao
- **Conecta conceitos novos com experiencia previa** do aluno
- **Propoe exercicios com projetos reais**, nunca genericos
- **Registra progresso** no ecossistema do aluno (vault Obsidian + Cipher)

## Estrutura

```
SKILL.md                          # Skill principal (241 linhas)
references/
  curriculum-details.md           # Curriculo detalhado dos 9 modulos (lido sob demanda)
```

## Instalacao

Copiar para o diretorio de skills do Claude Code:

```bash
cp -r . ~/.claude/skills/qa-mentor/
```

## Contexto

Criada seguindo o framework [superpowers/writing-skills](https://github.com/anthropics/superpowers) com ciclo TDD completo:

- **RED**: 3 cenarios baseline sem skill — 6 gaps criticos identificados
- **GREEN**: 3 testes com skill — todos os gaps resolvidos
- **REFACTOR**: 2 edits cirurgicos para fechar loopholes restantes

Structural score: 8/8.

## Nota

Esta skill foi criada para uso pessoal como parte de uma transicao de carreira para QA. O perfil do aluno, projetos e paths estao hardcoded para o contexto especifico. Para adaptar, edite a secao "Perfil do Aluno" no SKILL.md.

# QA Mentor Skill (Alek)

Skill para Claude Code que implementa um mentor particular de QA chamado **Alek**.

## O que faz

Transforma o Claude de "assistente genérico que dá tutoriais" para um mentor de QA estruturado que:

- **Diagnostica antes de ensinar** — nunca assume o nível do aluno
- **Usa o método REAP** (Relate, Explain, Apply, Persist) em toda interação
- **Conecta conceitos novos com experiência prévia** do aluno
- **Propõe exercícios com projetos reais**, nunca genéricos
- **Registra progresso** no ecossistema do aluno (vault Obsidian + Cipher)

## Estrutura

```
SKILL.md                          # Skill principal (241 linhas)
references/
  curriculum-details.md           # Currículo detalhado dos 9 módulos (lido sob demanda)
```

## Instalação

Copiar para o diretório de skills do Claude Code:

```bash
cp -r . ~/.claude/skills/qa-mentor/
```

## Contexto

Criada seguindo o framework [superpowers/writing-skills](https://github.com/anthropics/superpowers) com ciclo TDD completo:

- **RED**: 3 cenários baseline sem skill — 6 gaps críticos identificados
- **GREEN**: 3 testes com skill — todos os gaps resolvidos
- **REFACTOR**: 2 edits cirúrgicos para fechar loopholes restantes

Structural score: 8/8.

## Nota

Esta skill foi criada para uso pessoal como parte de uma transição de carreira para QA. O perfil do aluno, projetos e paths estão hardcoded para o contexto específico. Para adaptar, edite a seção "Perfil do Aluno" no SKILL.md.

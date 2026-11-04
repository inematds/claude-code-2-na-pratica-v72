# Claude Code 2.0 na prática — curso INEMA v7.2

**🇧🇷 [Curso em português](https://inematds.github.io/claude-code-2-na-pratica-v72/) · 🇺🇸 [English](https://inematds.github.io/claude-code-2-na-pratica-v72/en/) · 🇪🇸 [Español](https://inematds.github.io/claude-code-2-na-pratica-v72/es/)**

As novidades do Claude Code para quem não programa, em sete aulas curtas, abertas e gratuitas. Cada novidade é testada num trabalho real (o curso de planilhas da Carla), com prompt pronto, prática com "pronto quando" e teste comentado. O curso diz o que é prévia, beta ou só nos EUA. "Claude Code 2.0" é o apelido das versões 2.1.x.

**Guia de consulta das 13 novidades (com os prompts):** https://inematds.github.io/claude-code-2/guia/

| # | Aula | Página |
|---|---|---|
| 1 | O mapa: o que mudou e o que já dá para usar | `aulas/mapa/` |
| 2 | Organizar: seções, side chat e split view | `aulas/organizar/` |
| 3 | Ajudantes: subagentes | `aulas/ajudantes/` |
| 4 | Apps e sites: computer use e navegador embutido | `aulas/apps-e-sites/` |
| 5 | Longe do computador: Remote Control, Projects e Duet | `aulas/longe/` |
| 6 | Entregar: Slides, Design, Dashboards e Docs | `aulas/entregar/` |
| 7 | Personalizar: comandos de barra e mods | `aulas/personalizar/` |

## O processo, do início ao fim

Legenda: 🧠 sessão com o Nei · ⚙️ script/timer · 🤖 `claude -p` / subagente

1. 🧠 Pedido do Nei + fatos conferidos na documentação oficial (`longrun/2026-11-01-claude-code-2/FATOS.md` no repo wifi).
2. ⚙️ Criar o curso: `~/.claude/skills/formato-curso-v72/scripts/novo-curso.sh ~/projetos/claude-code-2-na-pratica-v72 "Claude Code 2.0 na prática"`.
3. 🤖 Plano das aulas (`longrun/.../PLANO-AULAS.md`) → 3 redatores escrevem `conteudo/pt/aulas/*.json` (brief `longrun/.../BRIEF-AULAS.md`).
4. ⚙️ Imagens pelo Codex, uma por vez: `bash longrun/2026-11-01-claude-code-2/tools/imagens_curso.sh` (capa + fotos de abertura); capas EN/ES editando a original.
5. ⚙️ Portão: `python3 gerar.py && python3 validar.py --links && node ~/.claude/skills/formato-curso-v72/scripts/conferir-tela.cjs .`
6. 🤖 Revisor independente (agente novo, persona do público) → corrigir → revisar de novo; notas em `~/projetos/wifi/scripts/revisor-nota.py`.
7. ⚙️ EN/ES: `python3 ~/.claude/skills/formato-curso-v72/scripts/traduzir.py . en es` (tradutor central) → `gerar.py --lang en|es` → `validar.py --lang en|es` → conferir rótulos dos conferidores.
8. ⚙️ Publicar: commit (autor inematds) + `gh repo create inematds/claude-code-2-na-pratica-v72 --public --source . --push` + GitHub Pages da raiz.
9. 🧠 Vídeos (explicavideo 16:9 + 9:16 e rtex 9:16) → lives4, INEMA.CCODE, metritds; portal inema.club (skill `atualiza-portal`).

Conteúdo aberto e gratuito · [INEMA.CLUB](https://inema.club)

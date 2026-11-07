# art-director-skill

Skill de **Diretor de Arte + Diretor de Fotografia** para agentes de IA (Claude Code, Codex, Cursor e qualquer agente que leia `SKILL.md`). Ela dirige e revisa o visual de jogos, cutscenes e 3D em tempo real: enquadramento, movimentos de câmera, lentes (dolly zoom, DOF, bokeh), luz, paleta e um ciclo rigoroso de autocrítica com um crítico independente.

Funciona com qualquer engine: Unity, Unreal, Godot, Blender e three.js.

[Read in English](README.md)

## O que ela faz
- Lê primeiro a bíblia visual do projeto (`ART_DIRECTION.md`) e trata ela como lei. Se o projeto não tiver uma, oferece escrever a partir do modelo incluído.
- Descreve cada plano em 1 frase: lente, movimento, enquadramento e luz.
- Segue um pipeline de câmera: beats, stills de base, 2–3 coberturas, implementação e um **crítico independente** (outro modelo, só leitura, nota 1–5 por plano e "as cinco correções que importam"). Depois aplica as correções. São cerca de 5 rodadas.
- Revisa com rigor contra as suas referências. Cada achado vem como arquivo/cena, problema e correção.
- Planeja primeiro e depois pergunta: Continuar / Alterar / Acrescentar / Só o plano.

## Instalar

**Claude Code (todos os projetos):**
```bash
git clone https://github.com/stefanoferrao/art-director-skill.git
mkdir -p ~/.claude/skills
cp -r art-director-skill/art-director ~/.claude/skills/
```

**Claude Code (só um projeto):** copie `art-director/` para `<seu-repo>/.claude/skills/`.

**Outros agentes:** copie `art-director/` para a pasta de skills que o seu agente lê. Ou indique `art-director/SKILL.md` ao agente como arquivo de instruções.

Depois escreva `@art` ou peça coisas como "revise a câmera desta cutscene" ou "por que esta cena parece amadora?". A skill responde no seu idioma.

## Personalizar
Coloque o seu look em `ART_DIRECTION.md` na raiz do projeto (comece pelo `art-director/templates/ART_DIRECTION.md`). A skill continua genérica; o arquivo do seu projeto define paleta, luz e limites.

## Licença
MIT

# criativos-appyon

Skills do Claude para produzir os vídeos da Appyon (Auraly): o método do negócio, por cima da
base de criativos ([criativos-base](https://github.com/onunoszz-sudo/criativos-base)).

| Skill | O que faz |
|---|---|
| `appyon-producao` | manual de produção, prompts, processo de contas, referências e o perfil da conta `auraly-manifestacao` |
| `appyon-prehook` | monta o pre-hook do carro por script (`prehook.py`), com os sons de cada ação e os níveis da referência |
| `appyon-aprendizados` | regras aprendidas na produção (datas, legenda, pote hermético, tatuagens, elemento americano, hook por cortes), moldes validados (capacho → carro, bueiro, churrasqueira + "proof the universe"), copys, fluxo do Agente do Flow e conferência de takes |
| da base: `pesquisa-de-referencias`, `roteiro-e-copy`, `geracao-de-video-ia`, `edicao-de-video`, `qa-de-criativo`, `entrega-de-criativo` | o ciclo do vídeo, Flow em lote, QA e entrega |

## Instalar (uma vez)
Precisa de: Claude Code, acesso a este repositório e ao `criativos-base` no GitHub, `ffmpeg`
e Python 3 (`pip install pillow numpy faster-whisper`).

No Claude Code:
```
/plugin marketplace add onunoszz-sudo/criativos-appyon
/plugin install criativos@criativos-appyon
/plugin install appyon@criativos-appyon
```
Para atualizar depois: `/plugin marketplace update criativos-appyon`.

Sem `/plugin`: clone os dois repositórios e copie as pastas de `skills/` para `~/.claude/skills/`.

## Usar
Abra o Claude Code numa pasta de trabalho e peça em português, por exemplo:
- "faz o pre-hook do Noah com estes takes"
- "gera os 6 takes do vídeo de aquecimento do Liam no Flow, em lote"
- "cria o blueprint do avatar novo"

Os sons e a música (riser, snap, Interstellar) vêm do kit do David no Drive; não ficam aqui.

## Regras
- Nada é gerado no Flow ou no Dreamina sem dizer o custo em créditos e receber o "sim".
- O Claude não cria conta, não digita senha e não copia a planilha de contas.
- Os manuais são cópia do Cérebro do Pedro (`ferramentas/sincronizar_cerebro.py`): sugestão de mudança
  vai para o Pedro, não direto na cópia.

---
name: appyon-aprendizados
description: Regras e moldes aprendidos na produção diária dos vídeos dos avatares da Appyon (Kyle, Mary, Robert, Zack 2) em nov/2026 - datas da copy, legenda, pote hermético, tatuagens do blueprint, elemento americano no cenário, hook com cortes (sem acelerar ação), moldes validados (capacho → carro, bueiro à noite, churrasqueira + "proof the universe is listening"), copy C01 e copy nova, fluxo do Agente do Flow (aprovação, falhas, download) e conferência de take (frase exata, repetição no fim, sotaque, voz, segunda mão). Use em qualquer vídeo de avatar falando da Appyon, ao montar hook, ao gerar takes no Flow pelo Agente, ao conferir takes antes de montar, ou quando o usuário disser "faz o vídeo do bueiro", "formato da churrasqueira", "troca as datas", "confere os takes", "refaz o take".
---

# Aprendizados da produção (Appyon, nov/2026)

Complementa `appyon-producao` (manual do Cérebro). Aqui fica o que foi aprendido fazendo os vídeos,
com o feedback do David. Em caso de conflito com o manual, vale a regra mais recente daqui e a
dúvida vai para o David.

## O que ler, e quando
| Arquivo | Quando |
|---|---|
| `regras.md` | sempre, antes de gerar ou montar qualquer vídeo |
| `formatos.md` | ao escolher ou montar um molde (hook + falas) |
| `copys.md` | ao escrever ou trocar a fala (datas, frases da copy original) |
| `flow-agente.md` | ao gerar imagens e takes no Flow pelo Agente |
| `conferencia.md` | antes de montar: frase, repetição, sotaque, voz, mão, tatuagem |
| `estudo-de-formatos.md` | ao procurar formato novo no Instagram |
| `prompts/` | modelos de prompt (imagem base, hook, falas em 14 blocos) |
| `scripts/hook_cortes.py` | monta o hook por cortes (selfie → ação em 1,0x → flash) |
| `scripts/conferir_takes.py` | identifica o avatar do take, transcreve e compara com a copy |

## As 10 regras que mais derrubaram vídeo
1. A **primeira data** da copy é o dia da postagem. Vídeo entregue com data passada: avisar na hora.
2. **Frase exata**: o texto de referência vem do roteiro/prompt, nunca da transcrição do take.
3. O Whisper **engole repetição** no fim do take ("seal... seal"): conferir a energia do áudio.
4. **Sotaque**: "ACCENT LOCK" americano no prompt; o usuário confirma de ouvido.
5. Selfie: o avatar se filma em **handheld** o vídeo inteiro; a mão do celular nunca aparece.
6. Ação importante (abrir o pote, despejar) em **1,0x**; encurtar só com corte.
7. Pote de canela é **sempre hermético** (vidro, trava de arame, borracha laranja).
8. **Tatuagens só do blueprint**; na troca de pessoa, apagar as da imagem de origem.
9. **Elemento americano** visível em todo cenário (bandeira, futebol americano, picape).
10. **Legenda** na linha do olhar, logo abaixo do rosto, nunca em cima dele.

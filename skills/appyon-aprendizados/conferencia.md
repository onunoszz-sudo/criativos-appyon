# Conferência dos takes (antes de montar)

Erros que o David pegou e que a conferência automática deixou passar: sotaque britânico num take,
ordem das palavras trocada, palavra repetida no fim ("seal... seal", "everything... thing"),
"if" a mais no meio, "going to" no lugar de "gonna", segunda mão aparecendo, voz diferente no take 1.

## 1. Frase exata
- `scripts/conferir_takes.py <pasta>`: identifica o avatar pelo primeiro quadro, transcreve com o
  Whisper medium e compara palavra por palavra com a copy.
- O texto de referência é o do roteiro. Já houve take errado aprovado porque a referência tinha sido
  montada a partir da transcrição.
- Qualquer diferença (palavra trocada, faltando ou a mais) → refazer o take, x2.

## 2. Repetição no fim do take
- O Whisper costuma juntar a repetição na última palavra. Sinais: última palavra com mais de 0,6 s ou
  dois picos de energia separados por um vale; voz depois da última palavra.
- Transcrever só os últimos ~2 s com `initial_prompt="Transcribe every word verbatim, including
  repeated words."` ajuda, mas gera falso positivo no começo do trecho (palavra cortada).
- Repetição no fim, depois de uma pausa: cortar (`fim_max` no partes.json da montagem). Repetição no
  meio: refazer.

## 3. Voz e sotaque
- Distância de timbre de cada take contra a média dos outros do mesmo vídeo (espectro médio em dB):
  na rua à noite os aprovados ficaram em 0,31–0,46; no quintal 0,36–0,50 (ruído de fundo sobe o valor).
- Take bem acima dos outros (ex.: 0,65) soa como "outra voz": refazer x2 e ficar com o mais próximo.
- A pergunta do take 1 ("You want proof...?") sobe o valor em todos os avatares (~0,5): comparar com o
  mesmo take dos outros avatares antes de refazer.
- Sotaque não aparece nessa medida: ACCENT LOCK no prompt e o David confirma de ouvido.

## 4. Imagem
- Folha de 8 quadros por take (`ffmpeg -vf fps=8/duração,scale=90:160,tile=8x1`, um take por linha):
  segunda mão, mão do celular aparecendo, roupa e tatuagem iguais em todos os takes.
- Hook: folha a 2 fps para escolher a variação e a 4 fps para marcar os cortes. Conferir pote hermético,
  tampa abrindo só pela trava, POV na mesma luz (já veio POV de dia num hook noturno).

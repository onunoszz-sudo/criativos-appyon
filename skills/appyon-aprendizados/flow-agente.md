# Flow pelo Agente (o que funciona)

## Configuração
- Agente: engrenagem → Padrões de vídeo → **Omni 1.1 Flash, 9:16, x1**. "Confirmar antes de gerar"
  em Sempre. Conferir na resposta do Agente que ele diz "Omni 1.1 Flash em 9:16".
- Aprovar cada proposta no painel (**Approve**, nunca "Always approve"). Depois de clicar, conferir
  que só "Approve" ficou marcado.
- Confirmação sem resposta expira e a geração é cancelada.

## Mandar um pedido
1. Anexar a imagem pelo "+" da caixa do Agente → buscar o nome do arquivo em "Search assets" →
   clicar no item (ele entra direto como ingrediente).
2. Colar o prompt na caixa e conferir: tamanho do texto, uma palavra-chave do avatar e o ingrediente.
3. Mandar uma mensagem por pedido. Mandar outra enquanto o Agente ainda processa **cancela** a anterior.
4. Falas: um pedido com 14 blocos (BLOCO 1 completo; os outros "SAME PROMPT AS BLOCO 1, except: clip N;
   fala; tempo"). O Agente propõe em lotes (1, 2, 3, 4 ou todos de uma vez) e cada lote pede aprovação.
5. Conversa longa começa a dar "Something went wrong": abrir **sessão nova** do Agente para cada avatar.
6. Hook em modo elemento: "gere 2 vídeos usando a imagem anexada como ELEMENTO / REFERÊNCIA (NÃO
   como frame inicial)". Falas: a imagem é o FRAME INICIAL.

## Imagens (Nano Banana)
- Imagem não pede aprovação e não gasta crédito de vídeo.
- Para trocar a pessoa mantendo cena e roupa: anexar a imagem de cena e o blueprint, dizer qual é qual,
  e mandar **apagar as tatuagens da pessoa original**.
- Subir uma cópia com nome novo para cada uso: o Flow pode gravar a edição por cima do arquivo anexado.

## Falhas
- "Flow is experiencing high demand" e "We couldn't check your credits" não cobram. O "Retry" do card
  costuma falhar de novo: refazer pelo Agente só com os blocos que faltam (prompt com o primeiro bloco
  faltante completo e os outros referenciando ele).
- Em dia de sobrecarga, ~25% dos takes falharam na primeira passada.

## Baixar
- Menu do card (⋮) → Download → **720p** (Original size). Imagem: 1K.
- Lista é virtualizada: rolar em passos e baixar o que aparece; conferir por hash para não duplicar.
- O nome do arquivo não diz qual take é: identificar pelo primeiro quadro (igual à imagem base) e pela
  transcrição (`scripts/conferir_takes.py`).

## Prompts das falas
- Saem do **Gerador de Animação** da Appyon, uma vez por modelo de vídeo. A Movimentação vai numa frase
  só (o gerador quebra por "." e ";" e espalha pedaços entre os takes).
- Mesmo modelo para outro avatar: reaproveitar o prompt e trocar só avatar, voz e roupa.
- Quando o Gerador não abre, dá para adaptar a saída de um modelo existente trocando a Movimentação
  inteira (numa frase) nos dois lugares em que ela aparece e o bloco de áudio (ver `prompts/f27_falas_quintal_14blocos.txt`).

# Moldes validados e em teste

Todos: hook ASMR sem fala → flash branco → 13 ou 14 takes de fala (~1:40 no total), headline no topo
durante o hook, legenda de 2 a 3 palavras abaixo do rosto, música −14 dB.

## 1. Capacho → carro (campeão)
- **Hook:** na varanda, abre o pote hermético → close de cima só com mãos, pote, capacho e chão:
  levanta o capacho, despeja um monte grande de canela, solta e alisa → entra na picape (vista de
  fora, de lado) e a porta bate.
- **Falas:** dirigindo, carro sempre em movimento, ruído constante de estrada e motor.
- **Resultado:** os maiores alcances das páginas (3,6 mi, 1,6 mi, 560 mil, 394 mil views).
- Prompts: `prompts/k28_capacho.txt` (capacho), `prompts/e28_picape.txt` (entrada) e o modelo carro do
  Gerador de Animação para as falas.

## 2. Canela no bueiro (rua à noite)
- **Hook (3,4–3,8 s):** selfie à noite mostrando o pote (1,2x) → POV abrindo a trava (1,0x) → despejo
  da canela num bueiro de rua (1,0x) → flash.
- **Falas:** selfie handheld na mesma rua, embaixo da placa e do poste, segurando perto da boca o
  microfone do fone com fio branco. Áudio com ruído de rua à noite.
- **Resultado:** 233 mil views no primeiro teste da Mary.

## 3. "Proof the universe is listening" + churrasqueira (teste, nov/2026)
- **Origem:** estudo de formatos de manifestação com ≥ 1 mi de views (criador americano que fala em
  selfie, ao ar livre, com um exercício simples e "me conta o que mudou").
- **Hook (3,6–4,0 s):** selfie no quintal mostrando o pote (1,2x) → POV abrindo a trava (1,0x) →
  despejo da canela nas brasas da churrasqueira a carvão, ao lado de hambúrguer e salsicha (1,0x) →
  flash.
- **Falas:** 14 takes em selfie handheld no quintal, churrasqueira ao fundo, bandeira dos EUA na cerca,
  ambiente de quintal (passarinhos, vento, chiado da grelha). Copy em `copys.md`.
- **Mesma copy no molde 1:** capacho → picape → falas dirigindo (spec 028).

## Cortes do hook
`scripts/hook_cortes.py` recebe o take bruto e a lista de cortes `(início, fim, velocidade)`:
selfie curta a 1,2x, micro-corte na trava abrindo a 1,0x, despejo a 1,0x com fade branco no fim.
Os pontos de corte saem de uma folha de quadros a 4 fps (`ffmpeg -vf fps=4,tile=13x2`).

## O que não funcionou
- Dinheiro escondido (gaveta secreta, porta-luvas): 5 de 5 na base (146 a 5 mil views).
- Ritual de fumaça com pote de barro: viralizou, mas trouxe público fora dos EUA.
- Cartas de tarô "pick a card": formato de outro funil (soulmate) e místico demais para os avatares.

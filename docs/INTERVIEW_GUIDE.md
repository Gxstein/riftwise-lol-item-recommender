# Guia de estudo para a entrevista

Este documento acompanha o projeto para você aprender o código e explicar decisões com suas próprias palavras. Não memorize uma resposta pronta: use as perguntas para identificar lacunas e pratique explicando cada parte sem ler.

## Apresentação curta

> Riftwise é um protótipo em Python de recomendação explicável de itens para League of Legends. A primeira versão usa regras transparentes sobre o contexto da partida, e não um modelo treinado. Eu construí a separação entre dados, validação, recomendação e interface e avaliei o comportamento com cenários controlados.

Atualize essa fala para corresponder exatamente ao que o código fizer ao final.

## Perguntas que você deve conseguir responder

1. Qual problema o app resolve e quem o usaria?
2. Quais informações entram no recomendador?
3. Como uma regra transforma contexto em sugestão de item?
4. Como o sistema decide a ordem das sugestões?
5. O que significa a pontuação e o que ela **não** significa?
6. Como você tratou entradas incompletas ou inválidas?
7. Como verificou se as regras funcionam nos cenários planejados?
8. Quais são as limitações dos dados e como um patch novo afeta o app?
9. Por que a primeira versão não usa machine learning?
10. O que precisaria mudar para treinar e avaliar um modelo com dados reais?

## Conceitos para estudar junto com cada parte

- Python: funções, dicionários, listas, módulos, exceções e tipos simples.
- Engenharia: separação de responsabilidades, validação, logs e versionamento.
- Dados: esquema, origem, qualidade, atualização e rastreabilidade.
- Recomendação: sinais, regras, ranking, baseline e avaliação offline.
- ML: diferença entre heurística e modelo treinado; treino/teste; vazamento de dados; métricas adequadas ao objetivo.
- Produto: utilidade para a pessoa usuária, clareza das explicações e limites da recomendação.

## Como falar sobre uma limitação

Use uma estrutura factual: “Nesta versão, X é limitado por Y. Para melhorar, eu faria Z e mediria o resultado com W.” Não descreva planos futuros como funcionalidades já implementadas.

## Notas pessoais

Depois de cada etapa, acrescente aqui:
- O que aprendi:
- O que ainda não consigo explicar:
- Perguntas para revisar:

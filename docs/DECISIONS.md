# Decisões de projeto

## ADR 001 — começar com recomendação baseada em regras

**Estado:** aceita  
**Contexto:** o prazo de MVP é de duas semanas e o projeto está sendo construído como exercício de fundamentos. Não há ainda um conjunto de partidas rotulado e confiável para treinar um modelo.

**Decisão:** a primeira versão usa regras explícitas e uma pontuação heurística para ordenar itens. Cada sugestão deve mostrar quais sinais e regras contribuíram para ela.

**Consequências positivas:**
- O comportamento pode ser explicado durante uma entrevista.
- Casos de teste podem ser criados sem depender de serviços externos.
- É possível separar o que foi implementado do que seria uma evolução futura.

**Limitações:**
- As regras não aprendem automaticamente com partidas.
- A cobertura inicial será pequena e refletirá as decisões manuais do projeto.
- A pontuação não representa chance de vitória, taxa de sucesso ou qualidade estatística.

**Evolução:** comparar o baseline com um recomendador aprendido somente quando houver dados com licença e qualidade adequadas, além de uma avaliação offline definida.

## ADR 002 — usar dados estáticos versionados no MVP

**Estado:** aceita  
**Decisão:** começar com arquivos JSON locais e registrar patch, data de obtenção e fonte. Isso mantém o app simples e reproduzível.

**Consequência:** os dados não se atualizam sozinhos; a manutenção por patch será uma tarefa explícita.

## ADR 003 — não depender de scraping do OP.GG

**Estado:** aceita  
**Decisão:** o MVP não fará coleta automatizada do OP.GG. A fonte inicial para metadados estáticos será o Data Dragon da Riot; as regras didáticas terão sua própria documentação.

**Motivo:** reduzir dependências externas e evitar apresentar dados de terceiros como se fossem uma API pública oficial. Revisar políticas de uso antes de distribuir o produto.

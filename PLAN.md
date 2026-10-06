# Plano de desenvolvimento — 14 dias

**Período planejado:** 29/10/2026 a 11/11/2026  
**Ritmo estimado:** 1–2 horas por dia.  
**Regra de histórico:** cada commit será criado depois do trabalho correspondente, com data verdadeira. Se um dia for perdido, o plano pode ser deslocado; não vamos fabricar commits retroativos.

## Entrega final

Um app local que recebe campeão, rota e perfil da composição adversária, devolve itens ordenados e explica cada recomendação. A primeira versão será um baseline heurístico, não um modelo treinado.

## Cronograma

| Dia | Data | Trabalho | Commit planejado |
|---|---|---|---|
| 1 | 29/10 | Repositório, objetivo, escopo, arquitetura e documentação-base | docs: define Riftwise MVP and project plan |
| 2 | 30/10 | Estrutura Python, ambiente e instruções de execução | chore: initialize Python project structure |
| 3 | 31/10 | Dados versionados de campeões e itens | feat: add versioned champion and item data |
| 4 | 01/11 | Validação de dados e entradas | feat: validate recommendation inputs |
| 5 | 02/11 | Regras para dano físico, mágico, cura e resistência | feat: add matchup recommendation rules |
| 6 | 03/11 | Ordenação das sugestões e justificativas | feat: explain item recommendations |
| 7 | 04/11 | Testes de regras, entradas e casos extremos | test: cover recommendation scenarios |
| 8 | 05/11 | Tela inicial em Streamlit | feat: add Streamlit interface |
| 9 | 06/11 | Integração da interface com o recomendador | feat: connect UI to recommendation engine |
| 10 | 07/11 | Mensagens e validações para uso local | fix: handle invalid selections and empty results |
| 11 | 08/11 | Cenários offline para avaliar cobertura das regras | feat: add offline recommendation evaluation |
| 12 | 09/11 | Documentação de arquitetura, dados e limitações | docs: explain architecture and data sources |
| 13 | 10/11 | Revisão do fluxo e instruções de instalação | fix: polish MVP and setup instructions |
| 14 | 11/11 | Relatório de estudo e roteiro de apresentação | docs: add interview study guide and project report |

## Definição de pronto

- Uma pessoa consegue instalar dependências e iniciar o app seguindo o README.
- Entradas inválidas recebem uma mensagem clara.
- Cada item recomendado tem uma justificativa rastreável até uma regra ou dado.
- O conjunto de dados informa a versão do patch.
- Os cenários de avaliação e seus limites estão documentados.
- O README deixa explícito que o MVP não treinou um modelo de ML.

## Ajustes de prazo

O plano é um guia, não um compromisso de criar atividade em dias em que não houve trabalho. Se a rotina apertar, priorizar nesta ordem: recomendador funcionando, explicações, interface, avaliação e acabamento.

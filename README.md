# Riftwise

**Um recomendador explicável de itens para League of Legends, feito com Python.**

Riftwise é um projeto de portfólio e estudo de engenharia de IA. A primeira versão recebe um campeão, uma rota e uma composição adversária simplificada; então ordena sugestões de itens e explica as regras que influenciaram cada escolha.

> **Estado:** planejamento e fundação do projeto. O MVP será construído em 14 dias, com commits reais ao longo do trabalho.

## Objetivo

Demonstrar fundamentos de engenharia de software e IA aplicada: modelar dados, transformar contexto em recomendações, explicar decisões e avaliar o comportamento em cenários definidos.

A primeira versão é um **sistema de recomendação baseado em regras**. Ela não treina um modelo de machine learning e não deve ser apresentada como se treinasse.

## Escopo do MVP

- Catálogo pequeno e versionado de campeões e itens.
- Seleção de campeão, rota e perfil da equipe inimiga.
- Recomendações ordenadas com justificativa legível.
- Interface local simples em Streamlit.
- Cenários de avaliação reproduzíveis e documentação das limitações.

## Fora do escopo inicial

- Overlay durante partidas ou leitura da memória do jogo.
- Conta de jogador, login, dados de partidas ao vivo ou matchmaking.
- Treinamento de modelo ou alegações de que a build é “a melhor”.
- Coleta automatizada ou scraping do OP.GG.

## Fontes e dados

Dados estáticos de campeões e itens serão obtidos do [Data Dragon da Riot](https://developer.riotgames.com/docs/lol), com a versão do patch registrada junto dos arquivos. As regras de matchup serão pequenas, explícitas e documentadas como conteúdo didático do projeto.

O protótipo não depende de uma API pública do OP.GG. Se o projeto for publicado como produto para jogadores, será necessário revisar e cumprir as políticas de desenvolvedor da Riot, incluindo o registro do produto quando aplicável.

## Tecnologias planejadas

- Python
- Streamlit
- JSON para o conjunto inicial de dados
- Git e GitHub
- Testes automatizados para as regras do recomendador

## Executar

As instruções completas serão adicionadas quando a aplicação estiver implementada. O roteiro de desenvolvimento está em [PLAN.md](PLAN.md).

## Documentação

- [Plano de 14 dias e commits](PLAN.md)
- [Arquitetura e diagramas](docs/ARCHITECTURE.md)
- [Decisões de projeto](docs/DECISIONS.md)
- [Guia de estudo para entrevista](docs/INTERVIEW_GUIDE.md)

## Aviso

Riftwise é um projeto independente, educacional e não afiliado à Riot Games, League of Legends, OP.GG ou Blitz. Nomes e marcas pertencem aos seus respectivos titulares.

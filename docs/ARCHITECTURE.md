# Arquitetura do Riftwise

## Visão geral

A primeira versão separa a interface, a lógica de recomendação e os dados. Assim, as regras podem ser entendidas e avaliadas sem depender da tela.

~~~mermaid
flowchart LR
    U[Pessoa usuária] --> UI[Interface Streamlit]
    UI --> V[Validação de entrada]
    V --> R[Motor de recomendação]
    D[(Dados locais JSON<br/>patch registrado)] --> L[Carregador e validação de dados]
    L --> R
    R --> O[Itens ordenados + justificativas]
    O --> UI
    E[Cenários de avaliação] --> R
    R --> M[Relatório de cobertura das regras]
~~~

## Fluxo de recomendação

~~~mermaid
flowchart TD
    A[Selecionar campeão e rota] --> B[Informar composição inimiga]
    B --> C{Entrada válida?}
    C -- Não --> X[Mostrar como corrigir]
    C -- Sim --> D[Resumir ameaças e necessidades]
    D --> E[Aplicar regras explícitas]
    E --> F[Calcular pontuação heurística por item]
    F --> G[Ordenar sugestões]
    G --> H[Mostrar itens e motivos]
~~~

## Responsabilidades

| Parte | Responsabilidade |
|---|---|
| Interface | Coletar escolhas e apresentar recomendações |
| Validação | Detectar seleções ausentes ou inconsistentes |
| Dados | Guardar um conjunto pequeno, versionado e legível |
| Motor | Aplicar regras e produzir pontuações e justificativas |
| Avaliação | Executar cenários definidos e resumir cobertura |

## Contrato conceitual

**Entrada:** campeão, rota, adversários ou perfil agregado de ameaça.  
**Saída:** lista ordenada de itens, pontuação heurística e uma ou mais razões.

A pontuação serve apenas para ordenar as regras do protótipo. Ela não é uma probabilidade de vitória nem uma medida de força competitiva.

## Dados e atualização

Cada conjunto de dados deve indicar patch, data de obtenção e fonte. Não misturar itens de patches diferentes sem registrar essa diferença. Dados estáticos e recomendações serão mantidos separados para facilitar revisão.

## Avaliação

A avaliação inicial usa cenários pequenos escritos para cobrir situações como muita ameaça mágica, muito dano físico ou cura alta. Uma métrica de cobertura pode verificar se as recomendações incluem os tipos de resposta esperados nesses cenários. Ela não mede se a build vence partidas nem substitui avaliação com dados reais.

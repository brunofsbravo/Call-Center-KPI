# Call-Center-KPI
Um gerente no Call Center (Help Desk) quer um painel de KPI Mensal para acompanhar performance do time.

[Dashboard Call Center KPI (Tableau Public)](https://public.tableau.com/app/profile/bruno.bravo/viz/CallCenterHelpDesk-KPI/Painel1)

Este painel faz parte de um projeto realizado a partir de dados disponibilizados pela plataforma AnalystBuilder do Alex e tem como principal objetivo trabalhar os dados e apresenta-los no Tableau de forma a atender o seguinte contexto:

1. Um gerente no Call Center (Help Desk) quer um Painel de KPI Mensal (KPI do último mês e para usar nos meses seguintes);

2. Ele quer acompanhar o desempenho de seus funcionários, assim como algumas informações gerais sobre as chamadas;

3. Nosso objetivo é criar um painel para fornecer informações úteis sobre esses dados, mas ele não tem certeza exata do que deseja;

4. A ideia é primeiro criar um painel, apresentar ao gestor para um feeback e fazer as alterações conforme solicitado.

A fonte de dados disponibilizada, em Excel, tinha a seguinte estrutura:

![1](https://github.com/user-attachments/assets/87401a22-5070-4e0d-9664-f0220be08d45)

Primeiramente foram analisados todos os dados recebidos, limpar caso necessário e organizar de forma a conseguir montar um dashboard.
Nota-se que o arquivo original em excel possui uma coluna separada para informações de Data e Hora (Colunas C e D). Enquanto que o Tableau está juntando essas duas informações para uma única coluna de Data e Hora:

Foi necessário organizar a coluna de Data e Hora, já que ali tem informações importantes que seriam interessantes de avaliar separadamente. Para isso foi utilizado um campo calculado para retirar a Hora, utilizando o cálculo DATEPART('hour',[Time]).

![2](https://github.com/user-attachments/assets/96a4c015-7178-4bd3-973d-93a4f346a93f)

Foi feita a elaboração de cada planilha para colocar as "ideias no papel" e a partir daí foi ajustado conforme necessário.

## Organização do painel

- <ins>Satisfaction Rating</ins>

Este gráfico apresenta o Índice de Satisfação do Cliente, permitindo ao gerente avaliar a percepção dos clientes em relação aos atendimentos realizados pelos agentes no mês selecionado.

<img src="https://github.com/user-attachments/assets/412799fe-0eed-41a4-b298-195180695b66" width="350" />
</p>

- <ins>Call Volume During Week</ins>

Este gráfico informa o volume de chamadas em cada dia da semana no mês selecionado. Ele é essencial para oferecer uma visão geral e estratégica sobre a distribuição do fluxo de chamadas.

<img src="https://github.com/user-attachments/assets/3db1a609-c30a-41bb-a454-f5b62db882cb" width="700" />
</p>

- <ins>Resolution Rate</ins>

Este índice apresenta a taxa de chamadas resolvidas dentro do mês selecionado. É um parâmetro-chave para que o gerente avalie a eficácia dos agentes em atender e solucionar as demandas dos clientes.

- <ins>Calls per Day</ins>

De caráter informativo, este gráfico exibe o número total de chamadas realizadas ao longo do mês selecionado. Ele também pode ser usado para análises mais amplas, como a variação do volume de chamadas entre diferentes meses em um período anual.

- <ins>Average Call Length</ins>

Este gráfico informa a média de duração das chamadas no mês selecionado, auxiliando o gerente a compreender padrões de atendimento.

- <ins>Resolution by Agent</ins>

Este painel fornece uma visão detalhada do Índice de Resolução de Chamadas por agente, permitindo ao gerente avaliar o desempenho individual e realizar comparações entre os agentes.

<img src="https://github.com/user-attachments/assets/753fd26e-5d66-4ce2-a55d-532d2eb88150" width="350" />
</p>

- <ins>Resolved Calls by Agent</ins>

Este índice apresenta o número de chamadas resolvidas por cada agente, facilitando a comparação direta entre eles.

<img src="https://github.com/user-attachments/assets/87d3e78d-843b-4983-9ffc-59d9bd764a99" width="350" />
</p>

- <ins>Speed of Answer by Agent</ins>

Nesta tabela, o gerente pode avaliar a velocidade média de atendimento de cada agente, fornecendo mais um indicador para análise de desempenho.

<img src="https://github.com/user-attachments/assets/b54dea1b-1443-4b12-aa69-d735d866a3b6" width="350" />
</p>

- <ins>Destaques Visuais e Regras de Cores</ins>

Nas tabelas voltadas para a avaliação de agentes, os indicadores são destacados com cores baseadas em uma regra que considera a média entre o melhor e o pior desempenho. Resultados abaixo da média são exibidos em vermelho, enquanto os acima da média aparecem em azul, permitindo uma identificação rápida e visual dos desempenhos.

Além disso, os painéis são integrados de forma interativa, permitindo que o gerente selecione um agente específico ao clicar sobre ele e visualize todos os indicadores relacionados exclusivamente a esse agente. A mesma funcionalidade está disponível para dias da semana e índices de satisfação, oferecendo uma análise mais detalhada e personalizada.

- <ins>Dashboard</ins>

<img width="1269" alt="3" src="https://github.com/user-attachments/assets/42697f40-30ac-4ea6-a3e1-8395d1b44617"> 

Acesse o dashboard no formato de apresentação no seguinte link: [Dashboard Call Center KPI (Tableau Public)](https://public.tableau.com/app/profile/bruno.bravo/viz/CallCenterHelpDesk-KPI/Painel1)

## Pontos Observados

- Em março, o número total de chamadas foi de 1.612, com uma duração média de 3,6 minutos por chamada e uma taxa de resolução de 70,47%;

- O maior volume de chamadas ocorreu nas segundas-feiras, enquanto o menor foi registrado nas sextas-feiras;

- A maior parte das avaliações de satisfação dos clientes ficou entre 4 e 5, em uma escala de 0 a 5 pontos.

## Conclusões

- Em março, o agente Joe apresentou o pior desempenho entre os agentes, obtendo resultados abaixo da média nas três avaliações principais: velocidade de resposta, taxa de resolução e número de chamadas resolvidas. Embora seu tempo de resposta não tenha sido o pior, destacou-se como o agente que mais precisa de suporte e desenvolvimento em múltiplos aspectos;

- A agente Martha se destacou com o melhor desempenho geral, combinando uma alta taxa de resolução (78,74%), o maior número de chamadas resolvidas (163), porém registrou o maior tempo médio de resposta (72,55 segundos), o que indica que ajustes específicos podem ser necessários para melhorar sua eficiência no atendimento inicial;

- Apesar dos desafios com alguns agentes, a maioria das avaliações de satisfação ficou entre 4 e 5, refletindo um alto nível de aprovação geral dos clientes.

**Este dashboard destaca pontos fortes e áreas de melhoria, fornecendo ao gerente informações claras para ações estratégicas. Ele permite monitorar o desempenho de agentes específicos, como Joe e Martha, e ajustar treinamentos ou redistribuir tarefas para melhorar a eficiência e a experiência do cliente. Além disso, a análise dos dados mensais possibilita a otimização do planejamento da equipe, garantindo um atendimento mais ágil e de alta qualidade.
Com esses KPIs, a gerência terá uma visão abrangente e detalhada do desempenho mensal de cada agente, permitindo identificar pontos fortes, áreas de melhoria e tomar decisões estratégicas com base em dados concretos.**

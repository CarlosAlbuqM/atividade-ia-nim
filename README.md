Nim com Q-learning

IA que aprende sozinha a jogar Nim por aprendizado por reforço (Q-learning), jogando milhares de partidas contra si mesma.

Atividade enviada pelo Professor Aldo

O jogo
O jogo começa com quatro pilhas de objetos: 1, 3, 5 e 7.
Os jogadores se revezam. Em cada vez, o jogador tira um ou mais objetos de uma única pilha.
Quem tirar o último objeto perde.
O que foi implementado

Em nim.py, na classe NimAI:

Função	O que faz
get_q_value	Retorna o valor Q de um par (estado, ação), ou 0 se ele ainda não for conhecido.
update_q_value	Atualiza o valor Q com a fórmula Q(s, a) <- Q(s, a) + alpha * (nova estimativa - Q(s, a)).
best_future_reward	Retorna o maior valor Q entre as ações disponíveis em um estado, ou 0 se não houver ações.
choose_action	Escolhe uma ação pelo algoritmo epsilon-greedy: aleatória com probabilidade epsilon e, nas outras vezes, a de maior valor Q.
Como executar

É preciso ter o Python 3.12 ou mais recente. Não há dependências externas.

Para treinar a IA e jogar contra ela no terminal:

bash
python play.py

O programa treina a IA em 10.000 partidas e depois começa uma partida contra você. Na sua vez, informe o número da pilha (a contagem começa em 0) e quantos objetos quer tirar.

Testes
bash
python test_nim.py

Resultado: 51 de 51 testes passaram.

Estrutura
text
.
├── nim.py          # jogo e IA (funções implementadas)
├── play.py         # treina a IA e inicia uma partida
├── test_nim.py     # testes da atividade
├── instrucoes.md   # enunciado da atividade
└── README.md


Autor
Carlos Phelipe Mesquita de Albuquerque. Sistemas de Informação, CESMAC.

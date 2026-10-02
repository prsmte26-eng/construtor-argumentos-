Especificação — Construtor de Argumentos

**Status:** rascunho inicial  
**Público:** estudantes do 9º ano; uso individual em navegador  
**Produto:** jogo educacional web estático, em português do Brasil.

## 1. Contexto e objetivo

O jogo conduz o estudante por uma sequência de desafios de escrita: compreender uma situação, formular uma tese, selecionar razões e evidências, conectar ideias, redigir um parágrafo argumentativo e revisar a linguagem. A experiência prioriza aprendizagem e autoria, com feedback formativo.

### Alinhamento à BNCC

- **Foco declarado: EF09LP04** — escrever segundo a norma-padrão, usando estruturas sintáticas complexas no nível da oração e do período. O jogo deve praticar e revisar construção de períodos, pontuação e clareza em contexto significativo.
- **Habilidade associada: EF09LP03** — produção de artigo de opinião com posição, estrutura do gênero e tipos de argumento. Os desafios de tese, razões e evidências se alinham diretamente a esta habilidade.

O jogo não deve apresentar a EF09LP04 como se fosse, por si só, a habilidade de construir argumentos. A equipe docente/pesquisadora pode ajustar o recorte se a intervenção didática escolher outra habilidade como foco principal.

## 2. Usuários e necessidades

- **Estudante:** quer entender o desafio, experimentar ideias, receber orientação útil e revisar sem medo de errar.
- **Professor ou pesquisador:** precisa relacionar as atividades a objetivos curriculares observáveis e acompanhar a experiência sem expor estudantes.
- **Pessoa que acessa por tecnologia assistiva ou dispositivo limitado:** precisa completar o fluxo essencial com teclado, leitor de tela, zoom e conexão instável.

## 3. Escopo do MVP

### Incluído

- Tela inicial com objetivo, instruções e opção de iniciar.
- Sequência curta de missões: tese; escolha/avaliação de razões e evidências; conectores e organização de períodos; redação e revisão de parágrafo.
- Contexto de produção explícito e temas apropriados ao 9º ano.
- Feedback imediato em atividades objetivas e orientação formativa na atividade de escrita.
- Indicador de etapa/progresso e resumo final que destaque o que foi praticado e convide à revisão.
- Interface responsiva, acessível por teclado e adequada a leitores de tela nos fluxos essenciais.
- Execução sem backend, conta ou dependência de serviços externos. Conteúdo pode ser armazenado em arquivos locais do projeto.

### Fora do MVP

- Cadastro, autenticação, painel docente ou sincronização entre dispositivos.
- Correção automática integral de redações ou julgamento automatizado da qualidade de opiniões.
- Ranking público, chat, conteúdo gerado por usuários publicado na internet ou monetização.
- Garantia formal de conformidade WCAG sem auditoria e validação com usuários.

## 4. Histórias de usuário e critérios de aceitação

### US-01 — Compreender a atividade

**Como** estudante do 9º ano, **quero** saber o que vou praticar e como avançar, **para** começar com confiança.

**Aceitação**

- Dada a tela inicial, quando ela é exibida, então apresenta objetivo em linguagem clara, instrução principal e botão “Começar”.
- O objetivo menciona revisão da escrita (EF09LP04) e, quando a atividade envolve tese e argumentos, identifica EF09LP03 como habilidade associada.
- O estudante consegue iniciar usando teclado e o foco fica visível.

### US-02 — Formular uma tese

**Como** estudante, **quero** escolher ou escrever uma posição sobre uma questão, **para** aprender a apresentar uma tese clara.

**Aceitação**

- A missão informa tema, situação comunicativa e o que caracteriza uma tese para aquela tarefa.
- A resposta não é considerada errada por defender uma posição diferente dos exemplos.
- Se houver seleção de alternativas, cada alternativa tem texto compreensível e pode ser escolhida por teclado.
- O feedback explica se a posição responde à questão e oferece uma dica de revisão, sem impor opinião.

### US-03 — Sustentar a tese

**Como** estudante, **quero** relacionar razões e evidências à minha tese, **para** construir uma argumentação compreensível.

**Aceitação**

- A missão distingue razão (por que defendo a tese) de evidência/exemplo (o que sustenta a razão), com exemplo curto.
- O estudante pode associar ao menos uma razão a uma tese e justificar/identificar evidência pertinente.
- O feedback apresenta o critério aplicado; não afirma que uma opinião é falsa apenas por divergir de uma resposta modelo.
- Alternativas não dependem somente de posição visual ou cor para serem entendidas.

### US-04 — Articular ideias em períodos

**Como** estudante, **quero** experimentar conectores e estruturas de oração, **para** expressar relações entre ideias com clareza e adequação.

**Aceitação**

- A atividade apresenta um contexto e explica a relação lógica trabalhada (por exemplo, causa, oposição ou conclusão).
- Quando o estudante escolhe uma opção inadequada, recebe explicação e pode tentar novamente.
- A prática contempla ao menos uma tarefa de pontuação ou estrutura sintática alinhada à EF09LP04.
- A orientação não descreve variedades linguísticas como inferiores; situa a norma-padrão conforme o contexto formal proposto.

### US-05 — Redigir e revisar um parágrafo

**Como** estudante, **quero** escrever e reler meu próprio parágrafo, **para** praticar autoria e revisão.

**Aceitação**

- Existe um campo de texto com rótulo acessível, instrução, limite orientador (se houver) e critérios de revisão visíveis.
- Os critérios convidam a verificar tese, relação entre razão e evidência, clareza do período e pontuação/norma-padrão pertinente à tarefa.
- O estudante pode editar a resposta antes de concluir e não é obrigado a enviar texto a um servidor.
- Se sugestões automáticas forem usadas, cada uma é identificada como sugestão, traz justificativa breve e pode ser ignorada.
- O jogo não atribui nota automática definitiva nem declara que o texto inteiro está correto com base em verificações parciais.

### US-06 — Receber retorno e tentar de novo

**Como** estudante, **quero** receber feedback respeitoso e uma nova oportunidade, **para** aprender com minhas escolhas.

**Aceitação**

- Feedback diferencia acerto/avanço de próximo passo e usa linguagem respeitosa.
- Em desafios fechados, informa por que a resposta atende ou não ao critério e oferece nova tentativa.
- Não há perda de progresso por errar nem cronômetro obrigatório.
- Mensagens de sucesso e erro são comunicadas em texto e anunciáveis por tecnologia assistiva.

### US-07 — Usar o jogo com diferentes formas de acesso

**Como** estudante que usa teclado, leitor de tela, zoom ou dispositivo móvel, **quero** operar as tarefas e compreender seus estados, **para** participar com autonomia.

**Aceitação**

- Todas as ações essenciais são alcançáveis e operáveis por teclado, com ordem lógica e foco visível.
- Controles possuem rótulos/nome acessível, instruções associadas e estados compreensíveis por leitor de tela.
- Texto pode ser ampliado a 200% sem perda de tarefa ou rolagem horizontal na apresentação padrão suportada.
- Contraste e significado não dependem exclusivamente de cor; botões têm áreas e textos compreensíveis em tela estreita.
- Não há áudio obrigatório, limite de tempo ou animação essencial sem alternativa/controle.

### US-08 — Concluir e refletir

**Como** estudante, **quero** ver o que pratiquei ao terminar, **para** escolher o que revisar depois.

**Aceitação**

- A conclusão resume as habilidades praticadas e oferece acesso à revisão ou reinício.
- O resumo não compara o estudante com outras pessoas.
- O progresso é apenas da sessão, salvo se uma versão futura explicar explicitamente outro tipo de armazenamento.

### US-09 — Entender privacidade

**Como** estudante, **quero** saber onde minha resposta fica, **para** escrever com segurança.

**Aceitação**

- Antes da primeira produção livre, a interface informa se o texto fica somente no dispositivo e se é apagado ao sair/recarregar.
- A versão MVP não transmite redações, identificadores ou telemetria a serviços externos.
- Se houver salvamento local, existe orientação clara para apagar os dados salvos.

## 5. Requisitos funcionais

- **RF-01:** apresentar as missões em sequência e permitir avançar após uma ação ou decisão explícita.
- **RF-02:** registrar progresso temporário na sessão atual e mostrar etapa atual.
- **RF-03:** oferecer instrução e feedback correspondentes a cada desafio, inclusive estado de tentativa novamente.
- **RF-04:** permitir escrita e edição de resposta livre antes de concluir.
- **RF-05:** oferecer resumo final e caminhos de revisão/reinício.
- **RF-06:** funcionar sem autenticação, backend e chamadas de rede para recursos essenciais.
- **RF-07:** declarar de forma correta o vínculo EF09LP04/EF09LP03 nos materiais e na interface pertinente.

## 6. Requisitos não funcionais

- **Usabilidade:** interface em português do Brasil, responsiva e com instruções concisas.
- **Acessibilidade:** atender aos princípios da Constituição e usar WCAG 2.2 AA como alvo para avaliação dos fluxos essenciais.
- **Desempenho:** carregar rapidamente em conexão escolar comum; limitar imagens e bibliotecas; manter o conteúdo essencial disponível sem dependências externas em tempo de execução.
- **Privacidade:** minimizar dados; atividade principal local; nenhum serviço analítico por padrão.
- **Compatibilidade:** navegadores modernos em computadores, tablets e celulares; degradação compreensível quando JavaScript estiver desativado.
- **Manutenibilidade:** separar conteúdo das regras da interface quando isso simplificar atualização pedagógica; manter HTML semântico e JavaScript legível.

## 7. Fluxo principal

1. Início e apresentação do objetivo.
2. Leitura de um cenário e formulação de tese.
3. Seleção/associação de razões e evidências.
4. Revisão de conectores e construção de períodos.
5. Escrita de parágrafo e auto revisão guiada.
6. Feedback, oportunidade de ajuste e resumo da sessão.

## 8. Pressupostos e questões de pesquisa

- O MVP é um protótipo de intervenção pedagógica, não um sistema de avaliação de alto impacto.
- A escrita livre pode permanecer apenas na memória da sessão; a equipe deve confirmar a política antes de pilotar com estudantes.
- A adequação das tarefas, temas, duração e linguagem deve ser revisada por docente de Língua Portuguesa e pesquisador responsável.
- Estudos com participantes devem seguir os procedimentos éticos e institucionais aplicáveis antes da coleta de dados.

## 9. Referências

Brasil, Ministério da Educação. Base Nacional Comum Curricular (BNCC), Língua Portuguesa, Ensino Fundamental — Anos Finais, habilidades EF09LP03 e EF09LP04.

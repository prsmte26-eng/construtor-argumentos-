Plano de implementação — Construtor de Argumentos

**Status:** plano inicial do MVP  
**Abordagem:** aplicação estática em HTML, Tailwind CSS e JavaScript no navegador.

## 1. Objetivo técnico

Entregar um protótipo funcional que execute as missões de escrita no navegador, sem servidor, conta ou build complexo. O jogo deve carregar conteúdo localmente, funcionar em telas pequenas e dar suporte ao fluxo acessível definido em `Constitution.md` e `spec.md`.

## 2. Pilha

- **HTML5 semântico:** estrutura, títulos, navegação, formulários, regiões de status e conteúdo.
- **Tailwind CSS:** utilitários para layout responsivo, tipografia, espaçamento e estados de foco. Para protótipo acadêmico, pode-se usar Play CDN durante desenvolvimento; para distribuição estável, compilar CSS localmente com CLI e servir arquivo estático versionado.
- **JavaScript estático (ES modules):** controle de estado da sessão, fluxo das missões, validações leves e feedback.
- **JSON ou objetos JS locais:** conteúdo de cenários, enunciados, alternativas, critérios e mensagens. Sem chamadas remotas no MVP.
- **Hospedagem:** qualquer servidor estático institucional ou local; o protótipo pode abrir em servidor de desenvolvimento simples. Evitar dependências de backend.

## 3. Estrutura sugerida

```text
construtor-argumentos/
├── index.html
├── src/
│   ├── app.js             # inicialização e coordenação do fluxo
│   ├── state.js           # estado em memória da sessão
│   ├── content.js         # missões e mensagens locais
│   ├── render.js          # renderização/atualização das telas
│   └── styles.css         # Tailwind compilado ou ajustes mínimos
├── assets/
│   └── (ícones locais, se necessários)
├── Constitution.md
├── spec.md
└── plan.md
```

Para um primeiro protótipo pequeno, os módulos podem ser reduzidos, mas separar conteúdo pedagógico da lógica facilita revisão por docentes sem alterar o fluxo do jogo.

## 4. Organização do estado

Manter em memória um objeto simples, por exemplo:

```js
{
  currentMission: 0,
  answers: {},
  completedMissions: [],
  feedback: null
}
```

Não persistir redações por padrão. Caso pesquisa ou uso em sala exija retomada, discutir e especificar previamente armazenamento local, aviso ao estudante, ciclo de vida e ação para apagar. Evitar analytics e identificadores no MVP.

## 5. Sequência de desenvolvimento

### Etapa A — Esqueleto navegável

- Criar `index.html` com idioma `pt-BR`, landmarks, hierarquia de títulos e pontos de montagem claros.
- Construir cabeçalho, área da missão, progresso textual, botões de avançar/voltar e resumo final.
- Estilizar com Tailwind mobile-first; manter foco claramente visível.

### Etapa B — Conteúdo pedagógico

- Criar pelo menos uma sequência completa: tese, razões/evidências, articulação sintática e escrita/revisão.
- Explicitar cenário, interlocutor e objetivo de cada proposta.
- Revisar conteúdo com professor/pesquisador e conferir distinção EF09LP04 e EF09LP03.

### Etapa C — Lógica e feedback

- Implementar transições de missão sem recarregar a página.
- Criar componentes simples para escolha, associação e campo de texto.
- Implementar feedback localizado e repetição de tentativas em atividades fechadas.
- Não aplicar correção linguística automática abrangente; qualquer regra heurística deve declarar seu limite e apresentar sugestão revisável.

### Etapa D — Acessibilidade e responsividade

- Garantir navegação completa por teclado, foco visível, rótulos, mensagens de estado anunciáveis e ausência de dependência exclusiva de cor.
- Conferir zoom, layout estreito, contraste e leitura com tecnologia assistiva.
- Manter controles nativos sempre que possível e respeitar redução de movimento caso haja animação.

### Etapa E — Publicação e documentação

- Gerar/servir CSS local para distribuição, se a versão de protótipo usou CDN.
- Publicar como arquivos estáticos em ambiente institucional.
- Incluir instruções de execução, política de dados do protótipo e limitações pedagógicas/técnicas.

## 6. Decisões de implementação

- Atualizar conteúdo em uma única região principal e mover o foco para o título da nova missão, sem prender o foco em componentes inesperados.
- Usar elementos nativos (`button`, `fieldset`, `legend`, `label`, `textarea`) em vez de controles customizados quando possível.
- Para feedback dinâmico, usar uma região `aria-live="polite"` de forma contida; não anunciar a tela inteira a cada mudança.
- Evitar temporizadores obrigatórios, animação essencial, drag-and-drop sem alternativa e conteúdo dependente de hover.
- Se o CSS vier de CDN, documentar que a disponibilidade da rede afeta o estilo; preferir assets locais na versão de pesquisa/pilotagem.
- Não inserir ferramenta de correção/IA externa sem rever privacidade, consentimento, validade pedagógica e requisitos institucionais.

## 7. Riscos e respostas

| Risco | Resposta de projeto |
|---|---|
| Confusão entre EF09LP04 e habilidade de argumentação | Relacionar explicitamente EF09LP04 à revisão sintática e EF09LP03 à produção de artigo de opinião. |
| Feedback automático simplifica demais a escrita | Limitar regras automatizadas; usar feedback explicável e preservar decisão do estudante. |
| CDN indisponível na escola | Distribuir CSS compilado localmente na versão de piloto. |
| Texto de estudante exposto ou perdido | Não transmitir nem persistir por padrão; explicar comportamento antes da escrita. |
| Barreiras de teclado/leitor de tela | Construir com HTML semântico e revisar cada missão com critérios de acessibilidade. |
| Temas ou exemplos enviesados | Revisar materiais com docente e adequar linguagem e contextos ao público local. |

## 8. Critérios de conclusão do MVP

- O fluxo completo pode ser iniciado, concluído e reiniciado em navegador moderno.
- Todas as histórias prioritárias de `spec.md` têm representação na interface.
- É possível completar as missões sem mouse e sem depender apenas de cor.
- A habilidade EF09LP04 aparece com redação e interpretação corretas; EF09LP03 é indicada quando se trabalha argumentação.
- Redações não são enviadas a serviços externos e qualquer retenção futura está explicitada antes de uso.
- Conteúdo e interface podem ser atualizados como arquivos estáticos.

## 9. Operação

Durante o desenvolvimento, servir a pasta por um servidor estático local para evitar diferenças de carregamento de módulos ES. Para distribuição, publicar `index.html`, JavaScript, CSS e assets em hospedagem estática. Não há migrações, credenciais ou configuração de servidor de aplicação no MVP.

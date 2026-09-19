# Kanban Task Manager

Projeto de estudos para criar um gerenciador de tarefas com HTML, CSS e JavaScript puro.

**Status:** planejamento. A aplicação ainda será desenvolvida.

## Objetivo

Organizar tarefas em três colunas: **A Fazer**, **Em Andamento** e **Concluído**.

## Funcionalidades planejadas

- Criar tarefas com título e prioridade (baixa, média ou alta).
- Mover tarefas entre as três colunas.
- Excluir tarefas.
- Salvar e recuperar tarefas usando `localStorage`.
- Adaptar o layout para computador e celular.

Os dados ficarão no navegador de cada dispositivo, sem sincronização entre usuários e sem banco de dados ou back-end.

## Arquivos a criar

| Arquivo | Responsabilidade |
| --- | --- |
| `index.html` | Formulário, três colunas e ligação com CSS e JavaScript. |
| `style.css` | Layout responsivo, cards e indicadores de prioridade. |
| `script.js` | Estado das tarefas, eventos, renderização e persistência. |

## Modelo de tarefa

```js
{ id: 1, titulo: 'Estudar Git', status: 'a-fazer', prioridade: 'alta' }
```

Status: `a-fazer`, `em-andamento` e `concluido`.

## Etapas de desenvolvimento

1. Criar HTML e formulário acessível.
2. Estilizar colunas e cards com CSS responsivo.
3. Criar array de tarefas e função `renderizarTarefas()`.
4. Implementar `adicionarTarefa()`, `moverTarefa()` e `excluirTarefa()`.
5. Implementar `salvarNoLocalStorage()` e `carregarDoLocalStorage()` usando a chave `kanban_tarefas`.
6. Testar e publicar no GitHub Pages.

As etapas estão detalhadas nas Issues deste repositório. Arrastar e soltar pode ser uma melhoria futura; botões ou um seletor de status são suficientes para a primeira versão.

## Cuidados na implementação

- Rejeitar títulos vazios ou apenas com espaços.
- Inserir títulos no DOM usando `textContent`.
- Carregar os dados antes da primeira renderização.
- Tratar dados inválidos e erros de leitura/escrita no armazenamento.
- Salvar e renderizar após adicionar, mover ou excluir.

## Começar no computador

```bash
git clone https://github.com/nivro5498/kanban-task-manager.git
cd kanban-task-manager
code .
```

Crie os três arquivos e abra `index.html` no navegador ou use o Live Server do VS Code. Não é necessário instalar dependências.

Para enviar suas alterações:

```bash
git add .
git commit -m "feat: criar estrutura inicial do Kanban"
git push
```

## Publicação

Depois de criar e testar `index.html`, configure **Settings → Pages → Deploy from a branch → main → / (root) → Save**. Use caminhos relativos para CSS e JavaScript.

O repositório pode existir antes do site: a aplicação só estará pronta quando os arquivos forem implementados e a publicação concluir.

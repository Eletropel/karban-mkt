# Eletropel — Kanban de Marketing

Painel web interno para organizar os trabalhos do setor de Marketing da **Eletropel Distribuidora de Auto Peças**.

> Versão atual: Kanban com arrastar e soltar reforçado e persistência local por navegador.

## O que o sistema faz

- Organiza os trabalhos em formato Kanban.
- Permite arrastar os cards entre as etapas.
- Controla prioridade: urgente, alta, normal e baixa.
- Permite definir prazo, responsável, categoria e observações.
- Destaca trabalhos atrasados e os que vencem hoje.
- Possui busca e filtros.
- Permite editar e excluir trabalhos.
- Faz backup dos dados em arquivo `.json`.
- Permite restaurar um backup.
- Funciona em computador, tablet e celular.
- Não precisa de servidor ou banco de dados para funcionar.

## Estrutura do Kanban

1. **Backlog** — trabalhos recebidos que ainda não entraram na fila.
2. **A Fazer** — trabalhos que já estão definidos para execução.
3. **Em Andamento** — trabalho atualmente sendo produzido.
4. **Aguardando** — depende de informação, aprovação, material ou retorno.
5. **Concluído** — trabalho finalizado.

## Como publicar no GitHub Pages

### 1. Crie ou abra o repositório

No GitHub, crie um repositório para o projeto.

### 2. Envie estes arquivos

A estrutura deve ficar assim:

```text
/
├── index.html
├── logo-eletropel.png
└── README.md
```

### 3. Ative o GitHub Pages

No repositório:

**Settings → Pages**

Em **Build and deployment**, selecione:

- **Source:** Deploy from a branch
- **Branch:** `main`
- Pasta: `/ (root)`

Salve.

Depois de alguns instantes, o GitHub vai disponibilizar o endereço do site.

## Dados e armazenamento

A versão atual utiliza **localStorage** do navegador. O status da coluna é salvo imediatamente ao soltar um card, portanto atualizar a página não deve devolver o trabalho ao Backlog.

Isso significa que os trabalhos ficam armazenados no navegador/dispositivo em que o sistema está sendo utilizado.

Exemplo:

- cadastrar no Chrome do PC → fica salvo naquele navegador;
- abrir no celular → não terá automaticamente os mesmos trabalhos.

Por isso existe o botão **Backup**, que gera um arquivo JSON. Esse arquivo pode ser restaurado pelo botão **Restaurar**.

### Importante

Se futuramente o objetivo for que **todo o Marketing da Eletropel compartilhe o mesmo Kanban**, com várias pessoas vendo e alterando os mesmos trabalhos, será necessário trocar o armazenamento local por um banco de dados/backend ou serviço de sincronização.

## Personalização

A identidade visual utiliza as cores principais da marca:

- Amarelo Eletropel
- Vermelho Eletropel
- Preto
- Branco

A logo utilizada pelo sistema está em:

```text
logo-eletropel.png
```

Para trocar a logo futuramente, basta substituir esse arquivo mantendo o mesmo nome.

## Recomendações de uso

Ao receber um novo pedido, coloque inicialmente em **Backlog**.

Depois:

**Backlog → A Fazer → Em Andamento → Aguardando → Concluído**

Use **Aguardando** quando o trabalho estiver parado por depender de outra pessoa, aprovação, conteúdo, produto, informação ou qualquer outro retorno.

Para trabalhos com prazo crítico, utilize **Urgente** ou **Alta**.

## Próximas evoluções possíveis

O projeto pode posteriormente receber:

- login de usuários;
- banco de dados compartilhado;
- atualização em tempo real;
- comentários nos trabalhos;
- anexos e links para arquivos;
- histórico de alterações;
- notificações de prazo;
- calendário de entregas;
- painel de produtividade;
- cadastro de membros do Marketing;
- permissões por usuário;
- integração com Google Drive ou outros serviços.

---

**Eletropel Distribuidora de Auto Peças**  
Sistema interno — Marketing

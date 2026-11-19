# Objetivo

Atue como desenvolvedor front-end especializado em React, interfaces responsivas, acessibilidade e experiência do usuário.

Crie exclusivamente o **front-end funcional de um MVP de gerenciamento de tarefas acadêmicas semanais**, utilizando o ambiente de desenvolvimento disponibilizado pelo Lovable.

A aplicação será utilizada por estudantes que precisam registrar, visualizar e acompanhar suas atividades acadêmicas, distinguindo tarefas pendentes de tarefas concluídas.

O problema a resolver é a dificuldade de organizar e acompanhar essas atividades em uma interface simples e centralizada.

**Diretrizes obrigatórias:**
- Construir uma interface visual moderna, limpa, intuitiva e responsiva.
- Priorizar o uso em dispositivos móveis.
- Implementar somente as funcionalidades descritas neste prompt.
- Utilizar dados simulados e estado local em memória.
- Garantir que as operações funcionem visualmente, sem backend.
- Identificar claramente a aplicação como uma demonstração com dados simulados.
- Não criar autenticação, banco de dados, serviços externos ou persistência.
- Não implementar funcionalidades adicionais por iniciativa própria.

O objetivo é entregar um protótipo navegável e interativo, adequado à validação visual e funcional do MVP.

# Páginas

## Página única: Gerenciamento de tarefas

A aplicação deve possuir apenas uma página principal, organizada em quatro regiões.

### 1. Cabeçalho

Apresentar:
- Nome da aplicação: "Minhas Tarefas".
- Texto descritivo: "Organize e acompanhe suas atividades acadêmicas".
- Identificação discreta e visível: "Demonstração com dados simulados".

Não incluir menus de navegação, perfil, autenticação ou acesso a outras páginas.

### 2. Formulário de tarefas

Criar um formulário para cadastrar novas tarefas.

Componentes:
- Campo "Título", obrigatório.
- Campo "Descrição", opcional, com suporte a múltiplas linhas.
- Botão "Adicionar tarefa".

Regras:
- O título não pode ser vazio nem conter apenas espaços.
- A descrição pode permanecer vazia.
- Ao cadastrar uma tarefa válida, ela deve aparecer imediatamente na lista.
- Toda nova tarefa deve iniciar com status "Pendente".
- Após cadastrar, o formulário deve ser limpo.
- Se a validação falhar, apresentar uma mensagem de erro junto ao campo correspondente.
- Os campos devem possuir rótulos visíveis.

### 3. Filtros

Apresentar três opções:
- Todas
- Pendentes
- Concluídas

Apenas um filtro pode estar ativo por vez.

O filtro selecionado deve possuir uma indicação visual e acessível.

### 4. Lista de tarefas

Exibir as tarefas utilizando uma organização visual consistente.

Cada tarefa deve apresentar:
- Título.
- Descrição, quando informada.
- Status atual: "Pendente" ou "Concluída".
- Controle para alterar o status.
- Ação "Editar".
- Ação "Excluir".

Diferenciar visualmente tarefas pendentes e concluídas, sem depender exclusivamente de cores.

Utilizar componentes reutilizáveis para manter consistência entre os itens.

## Componentes necessários

Organizar a interface em componentes independentes, conforme apropriado:

- Cabeçalho.
- Formulário de tarefa.
- Campo de entrada com validação.
- Filtros de status.
- Lista de tarefas.
- Item de tarefa.
- Formulário de edição.
- Diálogo de confirmação de exclusão.
- Mensagem de lista vazia.
- Indicadores visuais de carregamento e erro.
- Mensagens de feedback das operações.

Não criar componentes para funcionalidades fora do escopo.

# Comportamentos

## 1. Fluxo principal do usuário

O fluxo esperado é:

1. O estudante acessa a página principal.
2. Visualiza as tarefas fictícias disponíveis para demonstração.
3. Preenche o título e, opcionalmente, a descrição de uma tarefa.
4. Seleciona "Adicionar tarefa".
5. A tarefa aparece na lista com status "Pendente".
6. Pode editar ou excluir a tarefa.
7. Pode marcar uma tarefa como concluída.
8. Pode retornar uma tarefa concluída ao estado pendente.
9. Pode utilizar os filtros para visualizar somente as tarefas desejadas.

Todas essas ações devem ocorrer sem recarregar a página.

## 2. Criar tarefa

Quando o formulário possuir um título válido, adicionar a tarefa ao estado local e atualizar imediatamente a lista.

Quando o título estiver inválido, impedir o cadastro e apresentar uma mensagem acessível.

## 3. Editar tarefa

Ao selecionar "Editar":
- Abrir uma interface de edição da tarefa selecionada.
- Preencher o formulário com os valores atuais de título e descrição.
- Permitir alterar os dois campos.
- Disponibilizar as ações "Salvar" e "Cancelar".
- Aplicar a mesma validação de título utilizada no cadastro.

Ao selecionar "Salvar", atualizar imediatamente a tarefa.

Ao selecionar "Cancelar", descartar as alterações.

A edição não deve alterar o status atual da tarefa.

## 4. Excluir tarefa

Ao selecionar "Excluir":
- Apresentar um diálogo de confirmação.
- Informar claramente qual tarefa será excluída.
- Disponibilizar "Cancelar" e "Excluir tarefa".

Ao confirmar, remover a tarefa da lista em memória.

Ao cancelar, manter os dados sem alterações.

Nunca excluir uma tarefa sem confirmação.

## 5. Concluir ou reabrir tarefa

Cada tarefa deve permitir alternar entre:
- Pendente.
- Concluída.

A alteração deve atualizar imediatamente:
- O estado visual do item.
- O texto ou indicador de status.
- A lista exibida conforme o filtro ativo.

Uma tarefa concluída deve poder voltar ao estado pendente.

## 6. Filtrar tarefas

O filtro "Todas" deve exibir todas as tarefas existentes no estado local.

O filtro "Pendentes" deve apresentar somente tarefas pendentes.

O filtro "Concluídas" deve apresentar somente tarefas concluídas.

O filtro deve atualizar a interface imediatamente, sem requisições externas.

O filtro selecionado deve permanecer ativo após criar, editar, concluir ou excluir uma tarefa.

## 7. Dados simulados

Inicializar a interface com algumas tarefas acadêmicas fictícias, incluindo tarefas pendentes e concluídas.

Exemplos:
- Revisar conteúdo de matemática.
- Finalizar atividade de programação.
- Ler capítulo de história.
- Organizar anotações da semana.

Esses dados devem ser definidos localmente no front-end.

Requisitos:
- Não utilizar API.
- Não utilizar banco de dados.
- Não utilizar Supabase.
- Não utilizar Lovable Cloud para armazenamento.
- Não utilizar localStorage, sessionStorage ou IndexedDB.
- Não utilizar cookies para armazenar tarefas.
- Não implementar sincronização.
- Não afirmar que as informações foram salvas permanentemente.

As alterações devem existir apenas na memória da aplicação durante sua execução.

Ao recarregar a página, os dados iniciais simulados poderão ser restaurados.

## 8. Estados de interface

Implementar os seguintes estados:

**Estado padrão:** apresentar as tarefas simuladas e todos os controles principais.

**Lista vazia:** apresentar uma mensagem informativa quando não existirem tarefas no estado local.

**Filtro sem resultados:** informar que não existem tarefas correspondentes ao filtro selecionado.

**Erro de validação:** indicar o problema próximo ao campo inválido, permitindo correção.

**Carregamento demonstrativo:** disponibilizar uma representação visual de carregamento, sem realizar chamadas de rede nem criar atrasos artificiais no fluxo normal.

**Erro demonstrativo:** disponibilizar uma representação visual de falha, sem associá-la a serviços ou requisições inexistentes.

**Confirmação de exclusão:** apresentar um diálogo acessível antes da remoção.

**Feedback de sucesso:** comunicar de forma discreta quando uma tarefa for criada, atualizada, excluída ou tiver seu status alterado.

Os estados de carregamento e erro devem ser implementados como variações demonstrativas dos componentes, sem adicionar páginas, rotas ou controles de desenvolvimento à interface principal.

## 9. Responsividade

Adotar a abordagem mobile-first.

Em dispositivos móveis:
- Organizar os componentes verticalmente.
- Manter campos e botões confortáveis para interação por toque.
- Evitar rolagem horizontal.
- Garantir que títulos e descrições longos não quebrem o layout.
- Adaptar as ações dos itens para telas estreitas.
- Manter os filtros acessíveis e legíveis.

Em tablets e desktops:
- Utilizar uma largura máxima apropriada para a área principal.
- Centralizar o conteúdo quando houver espaço disponível.
- Aproveitar a largura adicional sem comprometer a legibilidade.
- Preservar a mesma hierarquia visual e as mesmas funcionalidades.

Verificar especialmente a interface nas larguras de 320 px, 375 px, 768 px e 1440 px.

## 10. Acessibilidade

Aplicar requisitos básicos de acessibilidade:

- Utilizar HTML semântico.
- Associar rótulos aos campos.
- Permitir navegação por teclado.
- Apresentar foco visível nos elementos interativos.
- Garantir contraste adequado entre texto e fundo.
- Não depender somente de cores para transmitir informações.
- Disponibilizar nomes acessíveis para botões e controles.
- Comunicar erros de validação de forma acessível.
- Utilizar controles apropriados para alteração do status das tarefas.
- Permitir fechar diálogos pela tecla Escape.
- Gerenciar corretamente o foco ao abrir e fechar diálogos.
- Permitir que mensagens importantes sejam percebidas por tecnologias assistivas.
- Respeitar a preferência do usuário por movimento reduzido quando houver animações.

Utilizar boas práticas compatíveis com WCAG 2.2 nível AA nos aspectos aplicáveis a esta interface.

# Limites

Este projeto é exclusivamente um MVP front-end.

**Não implementar:**
- Login ou cadastro de usuários.
- Autenticação e autorização.
- Perfis ou gerenciamento de contas.
- Backend.
- Banco de dados.
- Supabase.
- Lovable Cloud para armazenamento ou serviços de backend.
- API REST, GraphQL ou qualquer integração externa.
- Persistência local ou remota.
- Notificações ou lembretes.
- Calendário.
- Datas de vencimento ou agendamento.
- Prioridades de tarefas.
- Categorias ou etiquetas.
- Subtarefas.
- Anexos.
- Pesquisa textual.
- Ordenação personalizada.
- Painéis analíticos.
- Gráficos e relatórios.
- Compartilhamento de tarefas.
- Recursos colaborativos.
- Páginas adicionais.

Não inserir controles visuais que aparentem oferecer funcionalidades indisponíveis.

Não adicionar recursos que não estejam expressamente previstos neste prompt.

O resultado deve ser um front-end interativo, mas sem infraestrutura de armazenamento ou comunicação externa.

# Critérios de aceitação visual

## CA01: Estrutura e responsividade

**Dado** que o estudante acessou a aplicação,  
**Quando** visualizar a interface em um celular, tablet ou desktop,  
**Então** o cabeçalho, formulário, filtros e lista devem apresentar organização consistente, sem sobreposição de elementos ou rolagem horizontal desnecessária.

## CA02: Cadastro e validação

**Dado** que o estudante está no formulário de tarefas,  
**Quando** tentar cadastrar uma tarefa sem título válido,  
**Então** a interface deve apresentar uma mensagem clara de validação, sem adicionar a tarefa.

**E quando** informar um título válido e confirmar o cadastro,  
**Então** a nova tarefa deve aparecer imediatamente na lista como pendente.

## CA03: Edição e exclusão

**Dado** que existe uma tarefa cadastrada,  
**Quando** o estudante selecionar "Editar",  
**Então** a interface deve apresentar os valores atuais e permitir salvar ou cancelar alterações.

**E quando** selecionar "Excluir",  
**Então** deve ser apresentado um diálogo de confirmação antes de remover a tarefa.

## CA04: Status e filtros

**Dado** que existem tarefas pendentes e concluídas,  
**Quando** o estudante alterar o status de uma tarefa ou selecionar um filtro,  
**Então** a lista e os indicadores visuais devem refletir imediatamente o estado atualizado.

## CA05: Estados, acessibilidade e simulação

**Dado** que o estudante utiliza a aplicação,  
**Quando** navegar pelos controles usando teclado ou encontrar uma lista vazia, erro de validação ou estado demonstrativo,  
**Então** os elementos devem permanecer compreensíveis, acessíveis e visualmente consistentes.

A interface também deve identificar claramente o uso de dados simulados e não deve sugerir armazenamento permanente.

# Resultado esperado

Entregar uma aplicação front-end funcional e responsiva, com uma única página e componentes reutilizáveis.

Antes de considerar a implementação concluída, verificar que:
- Todas as operações previstas funcionam em memória.
- Os filtros refletem corretamente as alterações de status.
- A exclusão exige confirmação.
- Os estados de interface foram contemplados.
- Os dados simulados estão identificados.
- Não existe persistência de tarefas.
- Não existe integração externa.
- Não foram criadas funcionalidades adicionais.
- A interface pode ser utilizada com teclado e em dispositivos móveis.

Priorizar o funcionamento correto dos requisitos essenciais sobre elementos decorativos.

**Não implementar funcionalidades extras, mesmo que sejam comuns em aplicações de gerenciamento de tarefas.**
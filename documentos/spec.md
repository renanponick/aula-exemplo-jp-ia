Tenho uma especificação de MVP de lista de tarefas.
Transforme-a em um prompt para gerar somente o front-end no Lovable.
Inclua: usuário, problema, fluxo, componentes, estados de interface,
responsividade, acessibilidade e restrições do escopo.
NÃO adicione autenticação, serviços de banco ou integrações externas.
Use dados simulados claramente identificados.
Organize a resposta em: objetivo, páginas, comportamentos, limites
e critérios de aceitação visual.
Antes do prompt final, aponte lacunas ou contradições.

Atue como um analista de requisitos especializado em aplicações web, com foco na definição de produtos mínimos viáveis (MVPs).

**Contexto:** Uma pessoa estudante precisa organizar suas atividades acadêmicas ao longo da semana. Atualmente, enfrenta dificuldades para registrar, visualizar e acompanhar quais tarefas estão pendentes ou concluídas.

**Objetivo:** Elaborar uma especificação clara, objetiva e verificável para um MVP de aplicação web de gerenciamento de tarefas semanais, priorizando simplicidade, usabilidade e funcionalidades essenciais.

**Escopo funcional:**
- Criar tarefas com título obrigatório e descrição opcional.
- Visualizar todas as tarefas cadastradas em uma lista.
- Editar o título e a descrição de tarefas existentes.
- Excluir tarefas, mediante confirmação do usuário.
- Marcar tarefas como concluídas ou retorná-las ao estado pendente.
- Filtrar tarefas por status: todas, pendentes e concluídas.

**Restrições:**
- Não incluir autenticação ou gerenciamento de usuários.
- Não implementar notificações, lembretes ou funcionalidades adicionais.
- Não adicionar recursos fora do escopo definido sem identificá-los explicitamente como sugestões.
- Não presumir tecnologias, banco de dados ou mecanismos de persistência que não tenham sido especificados.
- Manter o escopo adequado a um MVP de baixa complexidade.

**Entregáveis:**

1. **Usuário e problema:** Descreva o perfil do usuário, suas necessidades e o problema que a aplicação pretende resolver.
2. **Requisitos funcionais:** Apresente uma lista numerada, identificada por RF01, RF02 etc., descrevendo comportamentos observáveis e verificáveis.
3. **Requisitos não funcionais:** Apresente uma lista identificada por RNF01, RNF02 etc., contemplando usabilidade, responsividade, acessibilidade e aspectos de qualidade relevantes.
4. **Fora do escopo:** Relacione explicitamente as funcionalidades que não serão desenvolvidas nesta versão do MVP.
5. **Critérios de aceitação:** Defina exatamente cinco cenários de teste utilizando o formato **Dado, Quando, Então**, contemplando as principais operações da aplicação.

**Diretrizes de qualidade:**
- Utilize linguagem objetiva, sem ambiguidades ou requisitos duplicados.
- Diferencie requisitos obrigatórios de recomendações.
- Identifique qualquer requisito adicional como "Sugestão", acompanhado de sua justificativa.
- Evite decisões de implementação que não sejam necessárias para a especificação.
- Garanta que os requisitos sejam consistentes com as restrições estabelecidas.
- Escreva critérios de aceitação que possam ser verificados por meio de testes funcionais.

**Formato de resposta:** Organize os cinco entregáveis em seções numeradas, utilizando tabelas para os requisitos funcionais e não funcionais, com identificador, descrição e prioridade. Não gere código nem implemente a aplicação.
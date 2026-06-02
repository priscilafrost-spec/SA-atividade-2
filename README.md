# SA-atividade-2
segunda etapa da SA

Grupo: FerroTrack
Nomes: Lara, Nicole, Priscila e Sofia
Link: figma:https://www.figma.com/design/wSWBzbLd5MtQOwz7rCruTF/Mockup-da-S.A.-Ferrorama?node-id=0-1&t=V5WCaaNsso5dVFOi-0
canva: https://canva.link/uqw74xx0m4kvn17 

O **FerroTrack** é um aplicativo de monitoramento ferroviário desenvolvido para atender a todos os públicos, incluindo pessoas com deficiência visual ou auditiva. Seu principal diferencial está na combinação de usabilidade, acessibilidade e praticidade, proporcionando uma experiência simples e eficiente para qualquer usuário. Com uma interface intuitiva e de fácil navegação, o aplicativo foi projetado para ser utilizado por pessoas de diferentes faixas etárias, garantindo inclusão e facilidade de uso em todas as suas funcionalidades.


Vamos **utilizar** tanto no **front-end** quanto no **back-end** HTML para a estrutura, CSS para a parte visual, JavaScript para a interatividade do site, Bootstrap para puxar os ícones e vamos pegar alguns códigos prontos do Framework para agilizar algumas partes do nosso site. 

**Seção 2**
FerroTrack/
│
|----README.md/
│    -documentacao.md
│
|----assets/
|     - logoFerrotrack.png
|     -imagemUsuarios.png
|     -icone
|
|
|----pages/
|     -index.html
|     -login.html
|     -cadastro.html
|     -dashboard.html
|     -sensores.html
|     -usuarios.html
|     -trens.html
|     -relatorios.html
|     -relatorioOperacional.html
|     -relatorioPassagens.html
|     -relatorioManutencao.html
|     -relatorioCargas.html
|
|
|-----css/
|      -global.css
|      -navbar.css
|      -cards.css
|      -tabelas.css
|      -botoes.css
|      -login.css
|      -cadastro.css
|      -dashboard.css
|      -sensores.css
|      -usuarios.css
|      -trens.css
|      -relatorios.css
|
|
|------js/
|       -dados.js
|       -dashboard.js
|       -sensores.js
|       -usuarios.js
|       -relatorios.js
|       -validacoes.js
│
└── index.html

**Explição**
A estrutura do projeto foi organizada em pastas separadas para facilitar o desenvolvimento, a manutenção e o trabalho em equipe. Dessa forma, cada tipo de arquivo possui um local específico, tornando o sistema mais organizado e fácil de compreender.

Por que foi organizado dessa forma?
A separação entre páginas, componentes, estilos, scripts e recursos visuais foi dividido assim poris ele vai permitir que os integrantes da equipe trabalhem simultaneamente em diferentes partes do projeto sem gerar conflitos. Além disso, quando for necessário corrigir erros ou adicionar novas funcionalidades, será mais fácil localizar os arquivos relacionados.

Por que separar CSS por componente e por tela?
Os arquivos CSS foram separados entre componentes e telas para deixar o projeto mais organizado. Os estilos dos componentes são usados em elementos que aparecem em várias páginas, como botões, menus e tabelas. Já os estilos das telas são usados apenas em páginas específicas, como Login ou Dashboard. Essa divisão facilita a manutenção do sistema, evita repetir código e permite fazer alterações mais rapidamente.

 Por que auth.js separado de dados.js?
 Essa separação torna o código mais organizado, facilita os testes e evita que um único arquivo fique muito grande e difícil de manter. Caso seja necessário alterar apenas o sistema de login, por exemplo, o desenvolvedor poderá trabalhar somente no auth.js sem afetar as demais funcionalidades.
 
 

 


**Seção 3 — Componentes reutilizáveis identificados**

**Botão Primário**
Onde aparece: Login, cadastro, usuários, sensores e pagamento.
Variações: Normal e desabilitado.

**Campo de formulário**
Onde aparece: Login, cadastro, sensores e pagamento.
Variações: Texto, senha e seleção

**Card de informações**
Onde aparece: Dashboard, trens, usuários e sensores 
Variações: Com ícone, números e status

**Header**
Onde aparece: Quase todas as telas
Variações: Apenas título ou título com ações

**Menu de navegação inferior**
Onde aparece: Dashboard, usuários, sensores e cliente 
Variações: Ícone ativo destacado

**Tabela/Listagem**
Onde aparece: Trens, usuários e relatórios
Variações: Quantidade de colunas diferentes

**Badge de status**
Onde aparece:Trens, tickets e usuários
Variações: Normal e desabilitado.

**Notificação/Alerta**
Onde aparece:Notificação e Dashboard
Variações:Informação ou aviso.

**Card de ticket**
Onde aparece:Tickets
Variações: Cores diferentes conforme status

**Modal de confirmação**
Onde aparece: Exclusão e ações importantes
Variações:Confirmar ou cancelar

**Seção 4**

**1 Tela** - Tela de Inicio, vai para a tela de login ou de cadastro dependendo de quer entrar com uma conta existente, ou quer se cadastrar;
**2 Tela** - Tela de Cadastro Permite o registro de novos usuários, ela depende dos componentesde formulário criados;
**3 Tela** - Tela de login reponsável pela autenticação dos usuários e acesso ás funcionalidades do app;
**4 Tela** - Dashboard Centraliza as informações do monitoriamento ferroviário e serve como base para a navegação entre as demais funcionalidades;
**5 Tela**  Tela de Tisckets, tela para comprar passagens;
**6 Tela** - Tela de pagamento, opções de pagamento ia pix, ou cadastrar cartão
**7 Tela** - Tela de Lista de Trens, Listagem dos trens monitorados. Essa tela fornece os dados para acessar informações mais detalhados;
**8 Tela** - Detalhes dos trens, possui a localização, Status operacional, velocidade e histórico dos trens;
**9 Tela** - Tela de alerta, informa os atrasos, falhas mecanicas e problemas na ferrovia;
**10 Tela** - Tela de usuários, tela para perquisar usuários que ultilizam o app, sendo gestor, maquinista ou cliente;
**11 Tela** - Tela de Perfil, mostra as informações pessoais e alteração de senha;
**12 Tela** - Tela de Configuração, mostra notificações, privacidade e segurança e preferencia do sistema;
(13 espaço de menu, tem as opçõess de inicio, menu, estoque e funcionários).

## Justificativa
A implementação segue uma ordem baseada nas dependências técnicas do sistema. Primeiro são criados os componentes reutilizáveis, depois as telas de autenticação e acesso, seguidas pelas funcionalidades principais de monitoramento e consulta de dados. Isso garante uma construção organizada, reduzindo retrabalho e facilitando os testes durante o desenvolvimento.


**Seção 5**
## Fluxo 1: Login de usuário já cadastrado
Tela inicial → clica em "Entrar"
Inserir nome de usuário e senha (ou continuar com o google)  →  Clicar em "Entrar"

## Fluxo 2: Cadastro de usuário não cadastrado
Tela inicial  →  clica em "Entrar"
Preencher "Nome"  →  "Data de Nascimento"  →  "E-mail"  →  "Nome de usuário" (usuário deve escolher o nome que ele quer ser chamado)  →  Escolher perfil (cliente, gestor, maquinista)  →  "Senha"  →  "Confirmar senha"  →  "Salvar"

## Fluxo 3: Cadastro do gestor
Depois que o gestor acabar de fazer o fluxo 2 ele vai ser direcionado para outra tela
Preencher "Matrícula Profissional"  →  "Empresa Ferroviária"  →  "Região de atuação"  →  "Turno"  →  "N° de Identificação"  →  "CREA/Certifcação técnica"  →  "Senha"  →  "Confirmar Senha"

## Fluxo 4: Página inicial
Depois que o usuário fazer o cadastro ou login ele vai ser redirecionado para uma página de login inicial nela, contém os seguintes botões para o usuário escolher:

- Maquinista: Dashboard Geral, Gestão de Rotas, Monitoramento das Cargas, Manutenção dos Trilhos, Relatórios e Análises e Alertas e Notificações

- Gestor: Dashboard Geral, Gestão de Rotas, Monitoramento das Cargas, Manutenção dos Trilhos, Cadastro de Cargas, Relatórios e Análises, Alertas e Notificações, Cadastro de Cargas e Cadastro de Sensores

- Cliente: Dashboard Geral, Gestão de Rotas, Monitoramento das Cargas, Cadastro de cargas, Alertas e Notificações, Opções de Pagamento e Ticket de Viagem

## Fluxo 5: Tela de Tickets
Depois que o cliente clicar em "Ticket de Viagem" ele vai ser direcionado para uma tela contém:

- Campo de busca para escolher estação, linha ou destino de 

- Rotas favoritas de viagens (exemplo: Joinville → Curitiba)

- Partidas próximas (lugares que estão próximosa )

## Fluxo 6: Tela de pagamento
Depois que o usuário escolher o ticket de viagem dele, ele vai ser redirecionado para uma página de pagamentos, onde tem:

- Resumo da viagem: data, horário, passageiro, tipo de serviço, valor total

- Forma de pagamento: selecionar opção (cartão de crédito, pix, boleto, carteira digital)

## Fluxo 7: Dashboard
Depois que o usuário clicar na opção "Dashboard geral" na tela inicial, ele vai ser direcionado para uma tela onde contém:

- Um card informando o dia e como está o clima

- Um card "Meu Perfil" para o usuário poder ver o perfil dele

- Um card de "Documentação" 

- Um gráfico informando as rotas mais utilizadas no mês

## Fluxo 8: Perfil
Se o usuário clicar em "Meu Perfil" na tela de Dashboard, ele vai ser direcionado para a tela de perfil, que contém:

- A foto do perfil do usuário

- Nome do usuário

- E-mail, Telefone e Endereço

- Botão de "Sair"

## Fluxo 9: Gestão de Rotas
Depois que o usuário clicar na opção "Gestão de Rotas" na tela inicial, ele vai ser direcionado para uma tela onde contém:

- Um card informando alguns horários de trens

- Um card informando status de linhas (exemplo: Linha 555 está atrasada)

- Um card de alertas 

## Fluxo 10: Monitoramento de Cargas
Depois que o usuário clicar na opção "Monitoramento de cargas" na tela inicial, ele vai ser direcionado para uma tela onde contém:

- Mapa para visualizar as cargas e opção de "Adicionar rota"

## Fluxo 11: Alertas e Notificações
Depois que o usuário clicar na opção "Alertas e notificações" na tela inicial, ele vai ser direcionado para uma tela onde contém:

- Campo de busca para o usuário pesquisar alertas

- Dois cards de avisos mais importantes do dia (exemplo: rota x foi modeificada deivido à...)

## Fluxo 12: Adicionar Rotas
Na página de adicionar rotas o usuário deve seguir o seguinte fluxo:

- Selecionar o destino (campo para escolher a cidade) → Selecionar ponto de partida (campo para escolher a cidade) → Inserir data

Também tem um campo de "Excluir Rota", caso o usuário não queira mais uma rota específica

## Fluxo 13: Tela de sensores
Na tela de sensores o usuário deverá escolher uma das seguintes opções:

- Adicionar Sensor

- Remover Sensor

- Editar sensor

Após o usuário escolher alguma dessas opções, ele deve preencher os seguintes campos:

"Selecione o tipo de sensor" → "Selecione o local do sensor" → "Selecione a data da adição" ou "Selecione a data da remoção"  → "Descreva o procedimento"

## Fluxo 14: Páginas de usuário (somente gestor tem acesso)
Na tela de páginas de usuário, haverá 4 botões:

- Total de usuários (aparece todos os usuários)

- Usuários Ativos (aparece somente os usuários ativos)

- Usuários Inativos (aparece somente os usuários inativos)

- Usuários bloqueados (aparece somente os usuários bloqueados)

Nessas telas aparecerá "Buscar usuário" que a pessoa pode digitar o nome de algum usuário para procurá-lo, "Adicionar usuário" e lá no final tem "Bloquear" 

Em "Adicionar usuário" o gestor deverá preencher e seguir o seguinte fluxo:

Preencher "Nome completo" → "E-mail" → "Telefone" → Inserir "Foto de usuário" → "Nome de usuário" → "Senha temporária" → "Cargo" → "Permissões de acesso (selecionar quais permissões o novo usuário poderá ter acesso) → Marcar o status da conta do novo usuário (ativo ou inativo) → Clicar em "Salvar" para adicionar o novo usuário, ou em "Cancelar" se ele não quiser mais adicionar ele

## Fluxo 15: Página de Trens
Na página de trens, haverá dois botões:

- Lista de trens cadastrados: mostra o nome, ID e status dos trens cadastrados

- Informações básicas: mostra o local e a velocidade dos trens

## Fluxo 16: Relatórios
Na página de relatórios, haverá 4 botões:

- Relatórios operacionais: Mostra a quantidade de passagens que do dia, os horários das passagens, os trens atrasados, a média de atraso, e o total de viagens realizadas no dia

- Relatórios de Passagens: Mostra os lugares mais comprados e os tipos de tickets (meia, inteira, idoso)

- Relatórios de manutenção: Mostra o nome dos trens em manutenção, a data da manutenção e o tipo de manutenção

- Relatórios de carga: Mostra o tipo de carga, a data e o peso
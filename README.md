# 💻 CPFL ENERGIA - FLUXOGRAMA 

![CPFL-Imagem](https://fhinck.com/wp-content/uploads/2021/12/10169-blog-cases.png) <br>


# 📍 DESCRIÇÃO DO PROJETO <br>
Fluxo do sistema geral de solicitações e alocação de projetos da CPFL. Novas solicitações, suplementações, realocação de saldo, gestão da solicitação. Fluxo no Power Automate para gestão de aprovações. Listas no SharePoint para armazenamento e gerenciamento de dados.


# 🔜 FASE 3 → Fev/2025
Para  a fase 3, a ideia é desenvolver um sistema com 4 telas que identifica automaticamente qual é a permissão do usuário e direciona ele para a tela correta. Existem 4 níveis de permissão e acesso. <br> <br>
1️⃣ - Supervisor <br>
2️⃣ - Gerente <br>
3️⃣ - Diretor <br>
💻 - Administração <br>

## 1️⃣ TELA SUPERVISOR - POWER APPS
O supervisor ao acessar o sistema, verá  todas suas solicitações aprovadas e o valor total de todas elas. Ao clicar no botão de mais informações, ele verá todas as informações daquela solicitação, distribuição mensal, prévia, comprometido e linhas orçamentárias. Alguns campos são possíveis editar. <br>

- [x] 🟢 Filtro de Data 
- [x] 🟢 Filtro de Status 
- [x] 🟢 Filtro de Tipo
- [X] 🟢 Alinhamento de Design (Fases Anteriores)
- [X] 🟢 Galeria de Itens → Solicitações
- [X] 🟢 Botão de Clear
- [x] 🟢 Botão de Mais Informações
- [x] 🟢 Configuração de PopUp
- [x] 🟢 Label de Apoio (Countrow)
- [x] 🟢 Label de Soma
- [x] 🟢 Label de Filtros Aplicados
- [X] 🟢 Detalhes da Solicitação (PopUp)
- [ ] 🔴 Prévia ME (PopUp)
- [ ] 🔴 Comprometido (PopUp)
- [X] 🟢 Trava de Cálculo (PopUp)
- [X] 🟢 Distribuição Mensal (PopUp)
- [ ] 🔴 Linhas Orçamentárias (PopUp)

## 2️⃣ TELA GERENTE - POWER APPS
Basicamente a mesma tela do supervisor, porém, com foco em campos de justificativa, onde será 3 campos, e o gerente obrigatoriamente precisa preencher esses campos e enviar para o diretor (nível acima). Menos informações do que a tela de supervisor. <br>

- [x] 🟢 Galeria de Itens
- [x] 🟢 Filtro de Entidade
- [x] 🟢 Filtro de Data
- [x] 🟢 Botão de Clear
- [x] 🟢 Filtro de Planta
- [x] 🟢 Label Countrow
- [x] 🟢 Label Somatória
- [x] 🟢 Valor Orçamento
- [x] 🟢 PopUp Mais Informações
- [x] 🟢 Justificativa Orçamento x ME
- [x] 🟢 Justificativa Compromissado x ME
- [x] 🟢 Justificativa Real x Orçado
- [ ] 🔴 Real
- [ ] 🔴 Prévia
- [ ] 🔴 Orçamento x ME
- [ ] 🔴 ME

 ## 3️⃣ - TELA DIRETOR - POWER APPS
 
- [x] 🟢 Galeria de Itens
- [x] 🟢 Filtro de Entidade
- [x] 🟢 Filtro de Data
- [x] 🟢 Botão de Clear
- [x] 🟢 Filtro de Planta
- [x] 🟢 Label Countrow
- [x] 🟢 Label Somatória
- [x] 🟢 Valor Orçamento
- [x] 🟢 PopUp Mais Informações
- [x] 🟢 Justificativa Orçamento x ME
- [x] 🟢 Justificativa Compromissado x ME
- [x] 🟢 Justificativa Real x Orçado
- [ ] 🔴 Real
- [ ] 🔴 Prévia
- [ ] 🔴 Orçamento x ME
- [ ] 🔴 ME

## 💻 - TELA ADMINISTRAÇÃO - POWER APPS
- Arquivo de Carga
- Arquivo de Prévia
- Arquivo de Compromissado
- Consolidado das Justificativas
- Consolidado da ME
- Botão de Período de Ajustes

## 🛠️ FERRAMENTAS UTILIZADAS
🖥️ - Power Apps → Sistema <br>
⚙️ - Power Automate → Gestão de Aprovações <br>
📊 - SharePoint → Banco de Dados

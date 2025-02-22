# Projeto PowerApps – Tela do Supervisor (Fase 3) 📍

Bem-vindo à documentação do projeto para a **Tela do Supervisor**, uma ferramenta essencial para a gestão do orçamento CAPEX da diretoria de O&M. Este documento reúne todos os detalhes, desde os requisitos funcionais até o roadmap e o passo a passo do desenvolvimento.

---

## Sumário 📚
- [Visão Geral](#visão-geral-📍)
- [Requisitos da Tela do Supervisor](#requisitos-da-tela-do-supervisor-📋)
- [Componentes e Funcionalidades](#componentes-e-funcionalidades-📊)
- [Roadmap do Projeto](#roadmap-do-projeto-🚀)
- [Passo a Passo do Desenvolvimento](#passo-a-passo-do-desenvolvimento-🔧)
- [Considerações Finais](#considerações-finais-✨)

---

## Visão Geral 📍
Nesta fase, o objetivo é desenvolver uma tela robusta e intuitiva para o **Supervisor** (e **Gerente 1**) gerenciarem o orçamento CAPEX. Essa tela consolidará as movimentações realizadas na Fase 2 – incluindo a criação de ODIs e ajustes de saldo – e permitirá uma análise detalhada da curva mensal (realizado, prévia, compromissado) e dos desvios orçamentários (anual vs. ME, realizado vs. YTD e mensal).

**Abas Disponíveis:**
- **CAPEX (ODI)**
- **Sobressalente (ODS)**

---

## Requisitos da Tela do Supervisor 📋
A tela deve oferecer uma visão completa e integrada dos dados orçamentários, incluindo:

- **Navegação e Layout:**
  - Alternância entre abas (CAPEX e Sobressalente)
  - Filtros e controles intuitivos para refinar a visualização dos dados

- **Listagem Consolidada de Solicitações:**
  - Tabela principal com os campos:
    - **EMPRESA, PLANTA, ID RISCO, DESCRIÇÃO, VALOR, ORÇADO AJUSTADO, ME REVISÃO, DELTA, COMPROMISSADO, PRÉVIA, NÚMERO ODI**
  - Filtros para separar registros por tipo (ODI ou ODS)

- **Detalhamento das Informações:**
  - **Aba ME Revisão:**  
    - Tabela com a Curva de Distribuição de Solicitações  
    - Dados históricos do "Modelo Realizado.xlsx" e dados atuais/futuros do SharePoint
  - **Aba Compromissado:**  
    - Tabela com dados do "Modelo Compromissado.xlsx" (fornecedor, documento, item, valor, quantidade, material, denominação)
  - **Aba Prévia:**  
    - Tabela com informações do "Modelo Prévia.xlsx" (TP. Doc, Dt/lçto, Cl.custo, etc.)
  - **Aba Realizado:**  
    - Tabela detalhada dos dados do "Modelo Realizado.xlsx"
  - **Aba Solicitação (Saldos):**  
    - Exibição do ID da Solicitação e Distribuição Mensal

- **Listagem de Saldos:**
  - Integração de dados das fontes LinhasOrcamentarias e Solicitações ODI/ODS com as colunas:
    - **EMPRESA, PLANTA, ID RISCO, DESCRIÇÃO, VALOR, ID BUDGET**

- **Criação e Gestão de Fatos Novos:**
  - Formulário para inserção de novos fatos com os campos:
    - **EMPRESA, PLANTA, ID RISCO, DESCRIÇÃO, VALOR, ID BUDGET** (campo texto) e **DISTRIBUIÇÃO MENSAL**
  - Listagem dos fatos inseridos com opções de edição (somente a partir do mês atual) e exclusão

- **Análise dos Desvios Orçamentários:**
  - Indicadores visuais e gráficos para comparar:
    - Anual vs. ME
    - Realizado vs. YTD
    - Análise mensal de desvios

- **Integração de Fontes de Dados:**
  - Conexões com SharePoint, BD CAPEX e arquivos Excel (Modelos Compromissado, Prévia e Realizado)

---

## Componentes e Funcionalidades 📊

### Layout e Navegação
- **Cabeçalho e Rodapé:**  
  Elementos para identificação do aplicativo e navegação contextual.
- **Abas Interativas:**  
  - **CAPEX (ODI):** Exibe registros e detalhes específicos para ODI.  
  - **Sobressalente (ODS):** Exibe registros específicos para ODS.
- **Filtros e Controles:**  
  Permitem refinar os dados conforme critérios de tipo de registro, data, entre outros.

### Tabelas e Formulários
- **Listagem Principal de Solicitações:**  
  Tabela consolidada que oferece uma visão geral dos dados.
- **Tabelas Detalhadas:**  
  Seções para detalhamento dos dados:
  - **ME Revisão**
  - **Compromissado**
  - **Prévia**
  - **Realizado**
  - **Solicitação (Saldos)**
- **Formulário para Fatos Novos:**  
  Permite a inserção, edição e exclusão de novos registros em tempo real.

### Indicadores e Análises
- **Desvios Orçamentários:**  
  Gráficos e indicadores que facilitam a análise dos desvios entre os diferentes orçamentos.
- **Listagem de Saldos:**  
  Tabela que consolida informações para o monitoramento orçamentário.

---

## Roadmap do Projeto 🚀

### 1. Planejamento e Preparação
- 📌 **Revisão das Fases Anteriores:**  
  Validar funcionalidades das Fases 1 e 2.
- 📌 **Levantamento de Requisitos:**  
  Mapear fontes de dados e definir os campos a serem exibidos.
- 📌 **Esboço do Wireframe:**  
  Desenhar a estrutura da tela, definindo áreas de navegação e exibição de dados.

### 2. Configuração do Ambiente de Desenvolvimento
- 📌 **Preparação do Ambiente:**  
  Verificar versões e dependências no PowerApps.
- 📌 **Integração de Fontes de Dados:**  
  Conectar ao SharePoint, BD CAPEX e importar os arquivos Excel.
- 📌 **Configuração de Permissões:**  
  Assegurar que Supervisores, Gerentes e Administradores tenham acesso adequado.

### 3. Desenvolvimento da Interface
- 📌 **Layout Principal:**  
  Criar o cabeçalho, rodapé, navegação entre abas e filtros.
- 📌 **Implementação das Abas:**  
  Desenvolver a listagem de solicitações e aplicar os filtros específicos para ODI/ODS.

### 4. Desenvolvimento das Seções Detalhadas
- 📌 **Tabelas Detalhadas:**  
  Implementar as tabelas para ME Revisão, Compromissado, Prévia, Realizado e Solicitação.
- 📌 **Listagem de Saldos:**  
  Integrar dados das fontes LinhasOrcamentarias e Solicitações ODI/ODS.
- 📌 **Criação e Gestão de Fatos Novos:**  
  Desenvolver o formulário com funcionalidades de edição e exclusão.

### 5. Testes e Validação
- 📌 **Testes de Integração:**  
  Verificar as conexões e atualização dos dados.
- 📌 **Testes Funcionais e de Usabilidade:**  
  Garantir a navegação e funcionalidade correta da tela.
- 📌 **Correção de Bugs:**  
  Realizar ajustes conforme feedback dos usuários.

### 6. Documentação e Treinamento
- 📌 **Documentação Técnica:**  
  Atualizar os registros de mudanças e criar um guia do usuário.
- 📌 **Sessões de Treinamento:**  
  Realizar treinamentos com Supervisores e Gerentes e disponibilizar materiais de suporte.

### 7. Deploy e Monitoramento
- 📌 **Publicação em Produção:**  
  Realizar o deploy da nova tela no ambiente final.
- 📌 **Monitoramento Pós-Deploy:**  
  Acompanhar o desempenho, integridade dos dados e coletar feedback contínuo.

---

## Passo a Passo do Desenvolvimento 🔧

1. **Preparação Inicial:**
   - Revisar funcionalidades das Fases 1 e 2.
   - Levantar requisitos e definir o layout (wireframe).

2. **Configuração do Ambiente:**
   - Preparar o ambiente no PowerApps.
   - Configurar conexões com SharePoint, BD CAPEX e arquivos Excel.
   - Verificar permissões dos usuários.

3. **Desenvolvimento da Interface:**
   - Criar o layout principal com cabeçalho, rodapé e navegação entre abas.
   - Implementar filtros e a listagem principal de solicitações.

4. **Implementação dos Detalhes:**
   - Desenvolver as tabelas detalhadas para cada aba (ME Revisão, Compromissado, Prévia, Realizado e Solicitação).
   - Inserir o formulário para criação de novos fatos com opções de edição e exclusão.
   - Configurar a listagem de saldos e os indicadores de análise.

5. **Testes e Validação:**
   - Executar testes de integração e funcionalidade.
   - Realizar sessões de usabilidade e ajustar a interface conforme feedback.
   - Corrigir bugs e validar melhorias.

6. **Documentação e Treinamento:**
   - Atualizar a documentação técnica e criar um guia do usuário.
   - Conduzir treinamentos e fornecer materiais de suporte (vídeos, FAQs).

7. **Deploy e Monitoramento:**
   - Publicar a nova tela em produção.
   - Monitorar desempenho e integridade dos dados.
   - Coletar feedback para futuras melhorias.

---

## Considerações Finais ✨
A **Tela do Supervisor** é vital para uma gestão orçamentária eficiente, consolidando informações de múltiplas fontes e oferecendo uma análise detalhada dos dados. Com uma interface intuitiva e funcionalidades robustas, o aplicativo permitirá uma tomada de decisão mais ágil e informada. A colaboração contínua entre as equipes de desenvolvimento e os usuários finais é fundamental para o sucesso deste projeto.

*Última atualização: 2025-02-22*

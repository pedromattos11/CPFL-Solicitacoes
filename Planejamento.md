# 🖥️✨ Tela Supervisor 🚀

---

## 📋🎨 Galeria: "galeria_Solicitacoes" 📸

### 📊🔢 Colunas:
- ✅ **Empresa** 🏢
- ✅ **Planta** 🌿
- ✅ **ID Risco** ⚠️
- ✅ **Descrição** 📝
- ✅ **Valor** 💲
- ✅ **Orçado Ajustado** 🔄  
  *(Somatório da distribuição mensal daquela ordem)* ➕➖
- ✅ **ME Revisão** 🔍  
  *(Somatório da distribuição mensal revisada daquela ordem)* 🔢
- ✅ **Delta** ➖  
  *(Orçamento Ajustado - ME Revisão)* ➗
- ✅ **Compromissado** 🤝
- ✅ **Prévia** 👀
- ✅ **Número ODI** 🔢

---

## ❓💡 Ações ao Clicar em um Item

### 👉 Se o item for **ODI** 🎯
Exibir uma guia com as seguintes opções:
- **ME Revisão** 🔎
- **Compromissado** 🤝
- **Prévia** 👀
- **Realizado** ✅
- **Solicitação** 📥

### 👉 Se o item for **Saldo** 💰
Exibir uma guia com as seguintes opções:
- **ME Revisão** 🔍
- **Solicitação** 📩

### 👉 Se o item for **Fato Novo** 🌟
Exibir apenas uma guia:
- **ME Revisão** 🔎  
  *(Mostrar distribuição mensal e detalhes)* 📆

---

## ➕💥 Adicionando Fato Novo

Ao clicar no botão de adicionar fato novo, deverá aparecer uma tablist com 2 opções: **Fato Novo** e **Distribuição Mensal** 📊.

**Itens para inputar um fato novo:**
- **EMPRESA** 🏢
- **PLANTA** 🌿
- **ID RISCO** ⚠️
- **DESCRIÇÃO** 📝
- **VALOR** 💲
- **ID BUDGET** (livre) 🎫
- **SOMATÓRIA MESES** 🗓️
- **DISPLAYMODE.DISABLED** 🚫 → Botão 🛑

---

## 🔧🚀 Passo a Passo – Front-End

### Geral 🌐
- Criar botão de **Deletar Item** 🗑️  
  *Configurar como `DisplayMode.Parent.Edit` para Fato Novo.  
  **Observação:** Botão deve estar como `DisplayMode.Parent.Disabled` quando aplicável.* ⚙️
- Criar tablist de itens → `"tablist_Principal"` 🗂️
- Criar tablist **CAPEX - Sobressalente** → `"tablist_Categoria"` 💼

### Galeria 🖼️
- Ajustar o container → `"container_Colunas"` 📐
- Criar máscara invisível para a linha inteira → `mascara_Galeria` 🎭

### SharePoint 📤
- Base de dados para fato novo 💾
- Coluna **Empresas** 🏢
- Coluna **Planta** 🌱

### Ao Clicar no Botão **Fato Novo** ✨
- Criar botão **Fato Novo** 🌟
- Configurar a propriedade `Items` da **tablist_Principal** 🗒️
- Criar coluna de "Fato Novo" na tablist 📋
- Criar as colunas do formulário 📝
- Implementar trava de segurança 🔒
- Exportar lista de ODI e ODI/ODS Solicitações para as colunas **Empresa** e **Planta** 📊
- Criar listagem dos meses → Formatar com fase anterior 📆
- Criar botão de **Salvar** 💾 e **Cancelar Operação** ❌
- Criar label de edição com propriedade `Visible.True` → `"label_FatoNovo"` 🏷️

---

## 🎯 Ações Específicas na Galeria

### Ao Clicar em um Item do Tipo **ODI** 🎯
Alterar a propriedade `Items` da **tablist_Principal** para incluir:
> **ME REVISÃO, COMPROMISSADO, PRÉVIA, REALIZADO e SOLICITAÇÃO** 🚀

Dentro da tablist, para cada opção:

#### **ME REVISÃO** 🔎
- Criar uma tabela com a distribuição mensal do orçamento do **Número ODI** 📊.

#### **COMPROMISSADO** 🤝
- Criar uma galeria com as seguintes colunas:
  - **Descrição do fornecedor** 📝
  - **Número do documento** 🔢
  - **Item** 📦
  - **Valor** 💰
  - **Quantidade** 🔢
  - **Material** 🛠️
  - **Denominação** 📋  
    *(Base: Modelo Compromissado.xlsx)* 📄

#### **PRÉVIA** 👀
- Criar uma galeria com as seguintes colunas:
  - **TP DOC** 📄
  - **DT LCTC** 📆
  - **CL Custo** 💲
  - **Denom Classe Custo** 🏷️
  - **Doc Compra** 🛒
  - **Material** 🛠️
  - **Denominação** 📋
  - **Texto breve material** 📝
  - **QTD Entr** 🔢
  - **UML** 🔤
  - **Valor/MR** 💲
  - **Descr Fornecedor** 📝  
    *(Base: Modelo Prévia.xlsx)* 📄

#### **REALIZADO** ✅
- Criar uma galeria com as seguintes colunas:
  - **Mês** 📆
  - **TP DOC** 📄
  - **DT LCTC** 📆
  - **CL Custo** 💲
  - **Denom Classe Custo** 🏷️
  - **Doc Compra** 🛒
  - **Material** 🛠️
  - **Denominação** 📋
  - **Texto breve material** 📝
  - **QTD Entr** 🔢
  - **UML** 🔤
  - **Valor/MR** 💲
  - **Descr Fornecedor** 📝  
    *(Base: Modelo Realizado.xlsx)* 📄

#### **SOLICITAÇÃO** 📥
- Criar uma galeria com as seguintes colunas:
  - **ID da Solicitação** 🆔
  - **Distribuição mensal da solicitação** 📊  
    *(Base: Modelo Realizado.xlsx)* 📄

---

### Ao Clicar em um Item do Tipo **SALDO** 💰
Alterar a propriedade `Items` da **tablist_Principal** para incluir:
> **ME REVISÃO e SOLICITAÇÃO** 📑

Dentro da tablist para **Saldo**:

#### **ME REVISÃO** 🔍 *(Editável)*
- Criar uma tabela com a distribuição mensal **REAL** do orçamento do **ID Budget** da linha orçamentária 📆.

#### **SOLICITAÇÃO** 📩 *(Somente Visualização)*
- Criar uma tabela com a distribuição mensal **ORIGINAL** do orçamento do **Número ODI** 📊.

---

## 📞 Ajuste de Fatos Novos (24/02/2025) 🗓️

- Gerenciar as colunas de **Empresa** e **Planta** por entidade do supervisor → Campo **Choice** no SharePoint 🔧.
- Entidade → Empresa → Planta 🏢🌿
- Estética → Tablist 🎨

**Observações:**
- **TIPO SALDO:** Editável na opção de **ME REVISÃO** 📝
- **DENOMINAÇÃO:** `galeria_ODI_Compromissado` 🏷️
- Adicionar campo de **Planta** na galeria principal 🌿.
- Background: Sobrepor 🎭
- **ME** nunca pode ser maior que o valor ajustado → Implementar trava de segurança/aviso 🔒⚠️

---

## Ao Clicar no Botão **Submeter a ME** 📤

- Acionar gatilho para enviar um resumo da **ME** por e-mail para o supervisor e o Gerente 1 📧.
- Gerar um arquivo **xlsx** contendo:
  - **Tipo** 🏷️
  - **ID Budget** 🆔
  - **Empresa** 🏢
  - **Planta** 🌿
  - **ID Risco** ⚠️
  - **ODI** 🔢
  - **Descrição** 📝
  - **Ajustado** 🔄
  - **ME** 🔍
  - **Delta** ➖
  - **Compromissado** 🤝
  - Distribuições ajustadas ao longo dos meses 📆
- Adicionar um registro em uma nova lista do SharePoint chamada **RevisaoME** com todas as colunas acima 📋.

---

# 🚀 TELA DE GERENTE 1

## Objetivo 🎯
Visualizar as solicitações dos supervisores agrupadas por planta, com possibilidade de revisão dos valores e acesso ao detalhamento 🔍📊.

- **Aba:** Capex e Sobressalente  
  *(ODS → Sobressalente; ODI → Capex)* 💼

## Filtros 🔎
- **Data:** Por mês (mês de alocação da ME) → Salvar data 📆
- **Planta:** Seleção múltipla 🌿
- **Supervisor:** Seleção múltipla 👥

## Agregado por Planta (Formato: Tabela) 📊

### Colunas
- **Planta** 🌱
- **Orçamento Aprovado** 💵
- **ME** 🔍
- **Delta** ➖  
  *(Aprovado - ME)*
- **Justificativa** 📝
- **Real** 📊  
  *(Somatória do realizado por planta)*
- **Compromissado** 🤝  
  *(Somatória do compromissado por planta)*
- **Prévia** 👀
- **Total Compromissado** 🤝💼  
  *(Real + Compromissado + Prévia)*
- **Outro Delta** ➗  
  *(Total Compromissado - ME)*  
  *(Justificativa)*

- Distribuições:
  - **ME** 🔍
  - **Real do mês passado** 📆
  - **Orçamento aprovado mês passado** 💵
  - **Delta** ➖  
    *(Justificativa)*
  - **Aprovado YTD** 📊
  - **Realizado YTD** 📊
  - **Delta YTD** ➖

*(Obs.: Scroll lateral para visualização da distribuição mensal ajustada ao longo dos meses)*

- Adicionar registro em nova lista do SharePoint chamada **RevisaoME** com todas as colunas acima 📝.
- Cenários:
  - Gestor faz alteração 🔄.
  - Gestor recusa e o valor volta para o supervisor ↩️.
- Após alteração pelo gestor, na tela do supervisor aparecerá o valor inputado pelo gestor 👀.

## Justificativas 📝

- **Justificativa 1:**  
  *Aprovado x ME (Anual)* 🗓️
- **Justificativa 2:**  
  *ME x Compromissado (Anual)* 🤝
- **Justificativa 3:**  
  *Aprovado x Realizado (Mensal)* 📆
- **Justificativa 4:**  
  *Aprovado x Realizado (YTD)* 📊

## Detalhamento por Planta 🔍

### Tabela de Detalhamento das Solicitações 📋
- Mesma tabela do supervisor, filtrada pela planta selecionada 🌱.
- O gestor pode ajustar os valores informados pelo supervisor na própria aba 🔄.

### Formulário de Justificativas 📝

## Ao Enviar as Justificativas e Submeter o Formulário (Gerente 1) 📤

- Acionar gatilho para enviar um resumo da **ME** por e-mail para o Gerente 1 e o Gerente 2 📧.
- Gerar um arquivo **xlsx** contendo:
  - **Tipo** 🏷️
  - **ID Budget** 🆔
  - **Empresa** 🏢
  - **Planta** 🌿
  - **ID Risco** ⚠️
  - **ODI** 🔢
  - **Descrição** 📝
  - **Ajustado** 🔄
  - **ME** 🔍
  - **Delta** ➖
  - **Compromissado** 🤝
  - Distribuições ajustadas ao longo dos meses 📆
  - **Entidade** 🏢 *(aparecerá também no gatilho do supervisor)*
- Incluir também as justificativas e os agrupamentos *(informação que não consta no fluxo do supervisor)* 📋.

---

# 🚀 Tela Gestor 2

- Agrupamento por **Entidade** (ao invés de por planta) 🏢🔀.
- As colunas e variações serão iguais, porém as justificativas serão agrupadas 📊.
- Classificar cada justificativa conforme o gestor 🏷️.
- As justificativas virão agrupadas por entidades diferentes 🌐.

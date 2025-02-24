# 🖥️ **Tela Supervisor**

---

## 📋 **Galeria: "galeria_Solicitacoes"**

### 📊 **Colunas:**
- ✅ **Empresa**
- ✅ **Planta**
- ✅ **ID Risco**
- ✅ **Descrição**
- ✅ **Valor**
- ✅ **Orçado Ajustado** *(Somatório da distribuição mensal daquela ordem)*
- ✅ **ME Revisão** *(Somatório da distribuição mensal revisada daquela ordem)*
- ✅ **Delta** *(Orçamento Ajustado - ME Revisão)*
- ✅ **Compromissado**
- ✅ **Prévia**
- ✅ **Número ODI**

---

## ❓ **Quando o usuário clicar em um item e esse item for:**

### 👉 **ODI**: Mostrar uma guia com as seguintes opções:
- ✅ **ME Revisão**
- ✅ **Compromissado**
- ✅ **Prévia**
- ✅ **Realizado**
- ✅ **Solicitação**

### 👉 **Saldo**: Mostrar uma guia com as seguintes opções:
- ✅ **ME Revisão**
- ✅ **Solicitação**

### 👉 **Fato Novo**: Terá apenas uma guia:
- ✅ **ME Revisão** *(Mostrar distribuição mensal e detalhes)*

---

## ➕ **Adicionando Fato Novo:**
### Quando o usuário clicar no botão de adicionar fato novo, deverá aparecer uma tablist com 2 opções: Fato Novo e Distribuição Mensal; Itens que devem aparecer para inputar um fato novo:
- ✅ **EMPRESA**
- ✅ **PLANTA**
- ✅ **ID RISCO**
- ✅ **DESCRIÇÃO**
- ✅ **VALOR**
- ✅ **ID BUDGET** *(livre)*
- ✅ **SOMATÓRIA MESES**
- ✅ **DISPLAYMODE.DISABLED → BOTÃO**

---

## 🔧 **Passo a Passo → Front-End**

### **Geral**
- ✅ **Criar botão de Deletar Item**  
  *(Configurar como `DisplayMode.Parent.Edit` para Fato Novo.  
  **Observação:** Botão deve estar como `DisplayMode.Parent.Disabled` quando aplicável.)*
- ✅ **Criar tablist de itens** → `"tablist_Principal"`
- ✅ **Criar tablist CAPEX - Sobressalente** → `"tablist_Categoria"`

### **Galeria**
- ❌ **Ajustar o container** → `"container_Colunas"`
- ✅ **Criar Máscara invisível** para a linha inteira → `mascara_Galeria`

---

### SharePoint
- ✅ Base de dados fato novo
- ✅ Coluna empresas
- ✅ Coluna Planta


### **Quando o usuário clicar no botão _Fato Novo_**
- ✅ **Criar botão Fato Novo**
- ✅ **Configurar a propriedade `Items` da tablist_Principal**
- ✅ **Criar coluna de "Fato Novo"** na tablist
- ✅ **Criar as colunas do formulário**
- ✅ **Criar trava de segurança**
- ✅ **Exportar lista de listagem de ODI e ODI/ODS Solicitações para as colunas de Empresa e de Planta**
- ✅ **Criar listagem dos meses → Formatar com fase anterior** 
- ✅ **Criar botão de Salvar** e **Cancelar Operação**
- ✅ **Criar label de edição** com propriedade `Visible.True` → "label_FatoNovo"

---

### **Quando o usuário clicar em um item do tipo _ODI_ na galeria**
- ❌ **Mudar a propriedade `Items` da "tablist_Principal" para:**  
  `"ME REVISÃO, COMPROMISSADO, PRÉVIA, REALIZADO e SOLICITAÇÃO"`

#### Dentro da tablist, ações para cada opção:
- **ME REVISÃO:**  
  - ❌ Criar uma tabela com a distribuição mensal do orçamento do **Número ODI**

- **COMPROMISSADO:**  
  - ❌ Criar uma galeria com as seguintes colunas:  
    **Descrição do fornecedor, Número do documento, Item, Valor, Quantidade, Material, Denominação**  
    *(Base: Modelo Compromissado.xlsx)*

- **PRÉVIA:**  
  - ❌ Criar uma galeria com as seguintes colunas:  
    **TP DOC, DT LCTC, CL Custo, Denom Classe Custo, Doc Compra, Material, Denominação, Texto breve material, QTD Entr, UML, Valor/MR, Descr Fornecedor**  
    *(Base: Modelo Prévia.xlsx)*

- **REALIZADO:**  
  - ❌ Criar uma galeria com as seguintes colunas:  
    **Mês, TP DOC, DT LCTC, CL Custo, Denom Classe Custo, Doc Compra, Material, Denominação, Texto breve material, QTD Entr, UML, Valor/MR, Descr Fornecedor**  
    *(Base: Modelo Realizado.xlsx)*

- **SOLICITAÇÃO:**  
  - ❌ Criar uma galeria com as seguintes colunas:  
    **Mês, TP DOC, DT LCTC, CL Custo, Denom Classe Custo, Doc Compra, Material, Denominação, Texto breve material, QTD Entr, UML, Valor/MR, Descr Fornecedor**  
    *(Base: Modelo Realizado.xlsx)*

---

### **Quando o usuário clicar em um item do tipo _SALDO_ na galeria**
- ❌ **Mudar a propriedade `Items` da "tablist_Principal" para:**  
  `"ME REVISÃO e SOLICITAÇÃO"`

#### Dentro da tablist para Saldo:
- **ME REVISÃO:**  
  - ❌ Criar uma tabela com a distribuição mensal **REAL** do orçamento do **ID Budget** da linha orçamentária

- **SOLICITAÇÃO:**  
  - ❌ Criar uma tabela com a distribuição mensal **ORIGINAL** do orçamento do **Número ODI**
 
 - **AJUSTE DE FATOS NOVOS:**
 - Gerenciar as colunas de empresa e de planta por entidade do supervisor → Campo choice → SharePoint
 - Entidade → Empresa → Planta
 - Estética → tablist 

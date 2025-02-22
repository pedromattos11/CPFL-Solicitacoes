# 🖥️ Tela Supervisor

## 📋 Galeria: "galeria_Solicitacoes" 

### 📊 Colunas:
- Empresa
- Planta
- ID Risco
- Descrição
- Valor
- Orçado Ajustado (Somatório da distribuição mensal daquela ordem)
- ME Revisão (Somatório da distribuição mensal revisada daquela ordem)
- Delta (Orçamento Ajustado - ME Revisão)
- Compromissado 
- Prévia
- Número ODI

## Quando o usuário clicar em um item e esse item ser:

### ODI: Mostrar uma guia com as seguintes opções:
- ME Revisão 
- Compromissado
- Prévia
- Realizado
- Solicitação

### Saldo: Mostrar uma guia com as seguintes opções:
- ME Revisão
- Solicitação

### Fato Novo: Terá apenas uma guia:
- ME Revisão: Mostrar distribuição mensal e detalhes

## Adicionando Fato Novo:
### Quando o usuário clicar no botão de adicionar fato novo, aparecerá um form com as seguintes opções pra ele inputar:

- EMPRESA 
- PLANTA 
- ID RISCO 
- DESCRIÇÃO 
- VALOR
- ID BUDGET (livre)
- DISTRIBUIÇÃO MENSAL;

### Passo a Passo → Front-End

### Geral
- [ ] Criar botão de **Deletar Item** (DisplayMode.Parent.Edit) para quando for Fato Novo  
  - *Observação:* Botão deve estar configurado como (DisplayMode.Parent.Disabled) quando aplicável.
- [ ] Criar tablist de itens → `"tablist_Principal"`

### Galeria
- [ ] Ajustar o container → `"container_Colunas"`
- [ ] Criar Máscara invisível para a linha inteira → `mascara_Galeria`

### O que fazer quando o usuário clicar no botão **Fato Novo**?
- [ ] Criar botão **Fato Novo**
- [ ] Configurar a propriedade `Items` da tablist_Principal
- [ ] Criar coluna de "Fato Novo" na tablist
- [ ] Criar as colunas do formulário
- [ ] Criar botão de **Salvar** e de **Cancelar Operação**
- [ ] Criar label de edição com propriedade `Visible.True`

### O que fazer quando o usuário clicar em um item do tipo **ODI** na galeria?
- [ ] Mudar a propriedade `Items` da tablist_Principal para:  
  `"ME REVISÃO, COMPROMISSADO, PRÉVIA, REALIZADO e SOLICITAÇÃO"`
- [ ] C

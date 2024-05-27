# Classificação de Risco de Crédito

# 1. Descrição do projeto
- Em um mercado financeiro cada vez mais competitivo, a capacidade de avaliar com precisão o risco de crédito dos clientes é essencial para a sustentabilidade e o crescimento de qualquer instituição bancária. O banco Coderbank, comprometido em fornecer serviços financeiros de excelência, enfrenta o desafio de aumentar a precisão na avaliação do risco de crédito para minimizar perdas e maximizar a rentabilidade. Uma vez que, decisões equivocadas podem resultar em inadimplência, impactando negativamente os lucros e a reputação da instituição. O desafio reside em identificar quais clientes representam um risco de inadimplência mais elevado e ajustar as políticas de crédito de acordo com esses insights.

- Para abordar este desafio, nossa equipe embarcou em um projeto de Data Science com o objetivo de analisar e prever a inadimplência de crédito utilizando o dataset German Credit. Nossa abordagem incluiu várias etapas estratégicas:

1. Aquisição de Dados: Utilizamos o dataset German Credit, uma fonte rica em informações demográficas e financeiras dos clientes.
2. Data Wrangling: Realizamos um cuidadoso tratamento dos dados, incluindo a limpeza e a transformação das variáveis, para garantir a qualidade e a consistência necessárias para a análise.
3. Análise Exploratória de Dados (EDA): Exploramos as relações entre as variáveis, identificando padrões e insights que orientaram a modelagem preditiva.
4. Modelagem Preditiva: Desenvolvemos modelos de machine learning para prever a probabilidade de inadimplência de cada cliente.
5. Interpretação e Ação: Traduzimos os resultados técnicos em recomendações práticas para a alta gerência, visando otimizar as políticas de concessão de crédito.
   
**1.2 Problema e objetivos de negócio**
- Identificar quais fatores influenciam a inadimplência de clientes para melhorar a avaliação de risco de crédito.
- Construir um modelo de previsão de inadimplência.
- Identificar e compreender as principais variáveis que afetam a inadimplência.
- Fornecer insights para a alta gerência sobre perfis de risco.
  
  Para atingir tais objetivos buscamos responder às seguintes perguntas:
- Quais são os fatores determinantes para a inadimplência de crédito?
- Como características dos tomadores de crédito influenciam o risco de crédito?
- Qual é a distribuição de risco entre diferentes tipos de crédito?

# 2. Fonte do Dataset e Critérios de Seleção (Data Acquisition)
- Fonte do Dataset: Kaggle - German Credit Data (https://www.kaggle.com/datasets/uciml/german-credit)
Critérios de Seleção:
- Dataset contém informações detalhadas sobre clientes e histórico de crédito.
- Disponibilidade de variáveis relevantes para a análise de risco de crédito.

# 3. Descrição das variáveis utilizadas
   - idade: Idade do cliente.
     Tipo: Numérica.
     Comportamento: Pode variar de jovens a idosos. Analisar a distribuição para identificar qualquer tendência em relação à inadimplência.
     Importância: A idade pode influenciar a capacidade de pagamento, com diferentes faixas etárias apresentando diferentes perfis de risco.

   - sexo: Sexo do cliente (0 - masculino, 1 - feminino).
     Tipo: Categórica.
     Comportamento: Pode mostrar diferenças no comportamento de crédito entre homens e mulheres.
     Importância: Pode ser relevante para identificar padrões específicos de inadimplência por gênero.

   - trabalho: Tipo de emprego (1 - trabalhador desqualificado, 2 - trabalhador qualificado, 3 - oficial, 4 - altamente qualificado).
     Tipo: Categórica.
     Comportamento: Diferentes tipos de emprego podem estar associados a diferentes níveis de estabilidade financeira.
     Importância: Pode ajudar a entender como o tipo de emprego afeta a capacidade de pagamento.

   - situação_de_moradia: Situação de moradia do cliente (own - própria, rent - alugada, free - sem custo).
     Tipo: Categórica.
     Comportamento: Pode influenciar a capacidade de pagamento, pois quem possui casa própria pode ter mais estabilidade financeira.
     Importância: Importante para entender a estabilidade financeira do cliente.
     
   - poupança: Poupança (0 - little, 1 - moderate, 2 - quite rich, 3 - rich).
     Tipo: Categórica.
     Comportamento: Nível de poupança pode indicar a capacidade do cliente de lidar com emergências financeiras.
     Importância: Crucial para avaliar a solvência do cliente.

   - conta_corrente: Conta corrente (0 - little, 1 - moderate, 2 - rich).
     Tipo: Categórica.
     Comportamento: Saldo da conta corrente pode indicar a liquidez do cliente.
     Importância: Importante para avaliar a liquidez imediata do cliente.

   - montante_de_crédito: Montante de crédito.
     Tipo: Numérica.
     Comportamento: Varia amplamente. Importante analisar a distribuição para identificar faixas de valor mais comuns.
     Importância: Diretamente relacionado ao risco, pois montantes maiores podem representar maior risco.
   
   - duração: Duração do crédito em meses.
     Tipo: Numérica.
     Comportamento: Períodos mais longos podem estar associados a maior risco devido à incerteza futura.
     Importância: Períodos de crédito mais longos geralmente apresentam maior risco de inadimplência.

   - finalidade: Finalidade do crédito (car, furniture/equipment, radio/TV, domestic appliance, repairs, education, vacation, retraining, business, other).
     Tipo: Categórica.
     Comportamento: Diferentes finalidades podem ter diferentes níveis de risco.
     Importância: Pode ajudar a entender a motivação por trás do pedido de crédito e o risco associado.

   - risco: Classificação de risco do cliente (1 - good, 0 - bad).
     Tipo: Categórica.
     Comportamento: Indica se o cliente é considerado um bom ou mau risco de crédito.
     Importância: Variável alvo para a modelagem preditiva de inadimplência.
  
# 4. Pipeline de soluções
1.Entendimento do negócio.
2.Compreensão dos dados.
3.Preparação de dados.
4.Modelagem.
5.Validação.
6.Implantação.

## Apresentação da análise "Risco de Crédito".
- Após entrar no local que o arquivo esta publicado.
- Clique no botão de "Download" ou "Raw" para abrir o arquivo diretamente.
- [Arquivo](https://github.com/Andressaach/Risco-de-Credito/blob/main/Apresenta%C3%A7%C3%A3o.ppt)

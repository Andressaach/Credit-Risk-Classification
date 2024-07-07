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

## Limpeza de Dados
### Tratamento de Valores Ausentes:
- Identificamos e tratamos valores ausentes nas variáveis mais críticas.
- Valores ausentes foram preenchidos utilizando imputação com a mediana para variáveis numéricas e a moda para variáveis categóricas. Esse método foi escolhido para evitar distorções nos dados, preservando a distribuição original.

### Remoção de Outliers:
- Utilizamos o método de IQR (Interquartile Range) para identificar outliers. Os valores fora de 1,5 vezes o intervalo interquartil foram considerados outliers. Dependendo do contexto, os outliers foram removidos ou substituídos por valores mais próximos dentro do intervalo aceitável.

### Transformação de Variáveis:
- Variáveis como 'renda' e 'montante de crédito' foram transformadas utilizando logaritmo para reduzir a assimetria. Outras variáveis categóricas foram codificadas usando one-hot encoding.

### Normalização e Padronização:
- Variáveis contínuas foram normalizadas para o intervalo [0, 1] ou padronizadas para terem média 0 e desvio padrão 1, dependendo da necessidade do modelo.

### Verificação de Consistência:
- Revisamos os dados para garantir que não houvesse inconsistências lógicas (ex.: idade negativa, renda zero para clientes empregados).

## Segmentação de Registros
- **Perfil de Risco**: Clientes foram categorizados em diferentes níveis de risco (ex.: baixo, médio, alto) com base em variáveis como histórico de crédito e montante de crédito.
- **Faixas Etárias**: Os dados foram segmentados em diferentes faixas etárias para analisar como a idade influencia o risco de inadimplência.
- **Níveis de Renda**: A renda foi segmentada em diferentes intervalos para entender a relação entre capacidade de pagamento e inadimplência.
- **Status de Emprego**: Clientes foram categorizados com base na sua situação de emprego para avaliar o impacto da estabilidade de renda.
- **Status da Conta Corrente**: Os registros foram segmentados de acordo com o status da conta corrente (ex.: saldo positivo, saldo negativo) para identificar padrões de risco associados.

# 4. Pipeline de soluções
1.Entendimento do negócio.
2.Compreensão dos dados.
3.Preparação de dados.
4.Modelagem.
5.Validação.
6.Implantação.

# 5. Apresentação da análise "Risco de Crédito".
- Após entrar no local que o arquivo esta publicado.
- Clique no botão de "Download" ou "Raw" para abrir o arquivo diretamente.
- [Arquivo](https://github.com/Andressaach/Risco-de-Credito/blob/main/Apresenta%C3%A7%C3%A3o.ppt)

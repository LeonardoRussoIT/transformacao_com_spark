## Contexto do Projeto

Recebi uma base de dados que demanda algumas etapas cruciais de pré-processamento para garantir que os algoritmos de Machine Learning possam operar de maneira eficiente e precisa. A seguir, apresento as etapas-chave que estou realizando para otimizar a qualidade e a utilidade dessa base de dados.

## Transformações necessárias na base de dados

### 1 - Verificar o balanceamento da base de dados

Ao analisar os dados disponíveis, constatamos que a base de dados está equilibrada: o número de cancelamentos e assinaturas ativas é igual. Esta observação é crucial para determinar o tipo de modelo de Machine Learning a ser utilizado, bem como as métricas relevantes e a interpretação dessas métricas.

### 2 - Conversão das colunas de SIM/NAO para valores binários

Nossa próxima etapa é solucionar o problema identificado: várias colunas em nosso conjunto de dados são do tipo string, o que impossibilita o processamento pelos modelos. Para começar, vamos nos concentrar nas colunas com dados mais simples de transformar, representados por valores binários "Sim" e "Não". Esses valores serão convertidos para 1 e 0, respectivamente.

### 3 - Criação de variáveis dummy

Observamos que algumas colunas possuem mais do que duas opções de valores, caracterizando um tipo categórico. Por exemplo, a coluna "Internet" possui opções como "DSL", "FibraOptica" e "Não". Similarmente, a coluna "TipoContrato" contém valores como "Mensalmente", "UmAno" e "DoisAnos", enquanto a coluna "MetodoPagamento" engloba várias opções de métodos de pagamento, como "BoletoEletronico", "Boleto", "DebitoEmConta" e "CartaoCredito".

Para lidar com esses dados, vamos criar uma coluna para cada opção de valor dentro de uma categoria específica. Isso implica na criação de colunas distintas para cada tipo de conexão de internet, método de pagamento e tipo de contrato. Se um cliente possuir uma opção específica, atribuímos o valor 1 à respectiva coluna e 0 para as demais. Essa técnica é comumente conhecida como criação de variáveis dummy e é amplamente utilizada para lidar com dados categóricos em análises estatísticas e de machine learning.

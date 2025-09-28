
# 📖 Projeto de Ciência de Dados: Previsão de Preços para o Airbnb

## Visão Geral

Este projeto de Ciência de Dados tem como objetivo principal a construção de um modelo de machine learning capaz de prever o preço de diárias de imóveis anunciados na plataforma Airbnb.

A partir de um conjunto de dados com características de diversos imóveis (como localização, número de quartos, comodidades, etc.), foi treinado um modelo de regressão. Para facilitar a interação e o uso prático do modelo, foi desenvolvida uma aplicação web com Streamlit, onde o usuário pode inserir as características de um imóvel e receber uma estimativa de preço em tempo real.

## 🎯 Problema de Negócio

A precificação de imóveis em plataformas como o Airbnb é um desafio tanto para novos anfitriões quanto para os mais experientes. Definir um preço muito alto pode diminuir a taxa de ocupação, enquanto um preço muito baixo pode resultar em perda de receita.

Este projeto busca solucionar esse problema, fornecendo uma ferramenta baseada em dados que ajuda os anfitriões a:

  * Definir preços competitivos e alinhados com o mercado.
  * Entender quais características do imóvel mais impactam o valor da diária.
  * Tomar decisões estratégicas para maximizar a receita.

## 🛠️ Tecnologias e Ferramentas Utilizadas

  * **Linguagem de Programação:** Python 3
  * **Análise de Dados:** Pandas
  * **Machine Learning:** Scikit-learn (inferido pelo uso do `joblib`)
  * **Desenvolvimento da Aplicação Web:** Streamlit
  * **Serialização do Modelo:** Joblib

## ✨ Features do Modelo

O modelo foi treinado utilizando as seguintes características (features) do imóvel:

| Categoria | Feature | Descrição |
| :--- | :--- | :--- |
| **Numéricas** | `latitude`, `longitude` | Coordenadas geográficas do imóvel. |
| | `accommodates` | Número de hóspedes que o imóvel acomoda. |
| | `bathrooms`, `bedrooms`, `beds` | Quantidade de banheiros, quartos e camas. |
| | `extra_people` | Valor cobrado por pessoa extra. |
| | `minimum_nights` | Número mínimo de noites para reserva. |
| | `ano`, `mes` | Ano e mês da coleta de dados. |
| | `n_amenities` | Quantidade total de comodidades oferecidas. |
| | `host_listings_count` | Número de imóveis anunciados pelo anfitrião. |
| **Booleanas** | `host_is_superhost` | Se o anfitrião é um "Superhost". |
| | `instant_bookable` | Se o imóvel permite reserva instantânea. |
| **Categóricas**| `property_type` | Tipo do imóvel (Ex: Apartamento, Casa). |
| | `room_type` | Tipo do quarto (Ex: Casa/apto inteiro). |
| | `cancellation_policy`| Política de cancelamento (Ex: Flexível, Rígida).|

## 🚀 Como Executar o Projeto

Para executar a aplicação de previsão em sua máquina local, siga os passos abaixo:

**1. Clone o repositório:**

```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
cd nome-do-repositorio
```

**2. Crie um ambiente virtual e instale as dependências:**

É uma boa prática usar um ambiente virtual para isolar as dependências do projeto.

  * **Crie o ambiente virtual**
    ```bash
    python -m venv venv
    ```
  * **Ative o ambiente (Windows)**
    ```bash
    .\venv\Scripts\activate
    ```
  * **Ative o ambiente (Linux/macOS)**
    ```bash
    source venv/bin/activate
    ```
  * **Instale as bibliotecas necessárias**
    ```bash
    pip install pandas streamlit scikit-learn
    ```
    > **Dica:** Você pode criar um arquivo `requirements.txt` com o conteúdo abaixo e instalar tudo com `pip install -r requirements.txt`.
    ```plaintext
    pandas
    streamlit
    scikit-learn
    ```

**3. Execute a aplicação Streamlit:**

Certifique-se de que os arquivos `Deploy-Projeto-Airbnb.py`, `modelo.joblib` e `dados.csv` estão no mesmo diretório. Em seguida, execute o comando no seu terminal:

```bash
streamlit run Deploy-Projeto-Airbnb.py
```

Seu navegador será aberto automaticamente com a aplicação web em execução\!

## 📂 Estrutura do Repositório

```plaintext
.
├── Deploy-Projeto-Airbnb.py  # Script principal da aplicação Streamlit
├── modelo.joblib             # Arquivo do modelo de machine learning treinado
├── dados.csv                 # CSV com os dados originais (usado para obter a ordem das colunas)
└── README.md                 # Este arquivo
```

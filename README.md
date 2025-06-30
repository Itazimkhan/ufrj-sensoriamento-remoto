# 🌍 UFRJ Sensoriamento Remoto

![GitHub release](https://img.shields.io/github/release/Itazimkhan/ufrj-sensoriamento-remoto.svg) [![Release Info](https://img.shields.io/badge/Check%20Releases%20-%20Visit%20Here%20-%23007ACC)](https://github.com/Itazimkhan/ufrj-sensoriamento-remoto/releases)

---

## 📖 Sobre o Projeto

Este repositório contém projetos e análises focadas em Sensoriamento Remoto, desenvolvidas na Universidade Federal do Rio de Janeiro (UFRJ). A pesquisa e a análise de dados de sensoriamento remoto são essenciais para entender o meio ambiente, monitorar mudanças e aplicar essas informações em diversas áreas, como agricultura, urbanismo e conservação ambiental.

---

## 🚀 Começando

Para começar a usar este repositório, você pode baixar os arquivos necessários na seção de [Releases](https://github.com/Itazimkhan/ufrj-sensoriamento-remoto/releases). Execute os arquivos conforme as instruções fornecidas para cada projeto.

### 📋 Pré-requisitos

Antes de executar os projetos, verifique se você possui as seguintes ferramentas instaladas:

- Python 3.x
- Jupyter Notebook
- Google Earth Engine API
- Bibliotecas Python: `numpy`, `pandas`, `matplotlib`, `scikit-learn`, entre outras.

### 🔧 Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/Itazimkhan/ufrj-sensoriamento-remoto.git
   ```
   
2. Navegue até o diretório do projeto:
   ```bash
   cd ufrj-sensoriamento-remoto
   ```

3. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

---

## 🛠️ Estrutura do Repositório

O repositório é organizado da seguinte forma:

```
ufrj-sensoriamento-remoto/
│
├── notebooks/            # Notebooks Jupyter com análises
├── scripts/              # Scripts em Python e JavaScript
├── data/                 # Conjuntos de dados utilizados
├── results/              # Resultados das análises
└── README.md             # Este arquivo
```

---

## 📊 Análises e Projetos

### 1. Análise de Dados

Os notebooks contêm análises de dados que utilizam técnicas de regressão linear e visualização de dados. Você encontrará exemplos de como aplicar esses métodos em conjuntos de dados reais.

### 2. Sensoriamento Remoto

Os projetos focam em dados obtidos de satélites, como o satélite Planck. Usamos a API do Google Earth Engine para acessar e processar dados de imagens de satélite.

### 3. Visualização

A visualização de dados é uma parte crucial da análise. Utilizamos bibliotecas como `matplotlib` e `seaborn` para criar gráficos informativos que ajudam a interpretar os resultados.

---

## 📚 Tecnologias Utilizadas

- **Colab Notebook**: Para facilitar a execução de códigos na nuvem.
- **Google Earth Engine**: Para acessar e analisar dados de sensoriamento remoto.
- **Python 3**: Linguagem principal para scripts e análises.
- **JavaScript**: Usado em alguns projetos para visualizações interativas.
- **Bibliotecas de Ciência de Dados**: `pandas`, `numpy`, `scikit-learn`, entre outras.

---

## 🔍 Exemplos de Uso

### Exemplo 1: Análise de Regressão Linear

Um dos notebooks demonstra como aplicar a regressão linear em dados de temperatura e precipitação. O código é comentado para facilitar a compreensão.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Carregar dados
data = pd.read_csv('data/temperatura_precipitacao.csv')

# Preparar dados para regressão
X = data['temperatura'].values.reshape(-1, 1)
y = data['precipitacao'].values

# Criar modelo
model = LinearRegression()
model.fit(X, y)

# Previsões
predictions = model.predict(X)

# Visualizar resultados
plt.scatter(X, y)
plt.plot(X, predictions, color='red')
plt.title('Regressão Linear: Temperatura vs Precipitação')
plt.xlabel('Temperatura')
plt.ylabel('Precipitação')
plt.show()
```

### Exemplo 2: Processamento de Imagens de Satélite

Outro projeto utiliza a API do Google Earth Engine para processar imagens do satélite Planck e gerar mapas de vegetação.

```javascript
// Carregar imagem do satélite
var image = ee.Image('COPERNICUS/S2/20210901T100031_20210901T100619_T31TCH');

// Calcular índice de vegetação
var ndvi = image.normalizedDifference(['B8', 'B4']).rename('NDVI');

// Visualizar resultados
Map.centerObject(image, 10);
Map.addLayer(ndvi, {min: 0, max: 1, palette: ['blue', 'white', 'green']}, 'NDVI');
```

---

## 🧑‍🤝‍🧑 Contribuindo

Se você deseja contribuir com este projeto, siga estas etapas:

1. Faça um fork do repositório.
2. Crie uma nova branch (`git checkout -b feature/nome-da-sua-feature`).
3. Faça suas alterações e commit (`git commit -m 'Adicionando nova feature'`).
4. Envie para o branch (`git push origin feature/nome-da-sua-feature`).
5. Abra um Pull Request.

---

## 📄 Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## 🌟 Agradecimentos

Agradecemos a todos os colaboradores e à UFRJ pelo suporte e incentivo nas pesquisas de sensoriamento remoto. O conhecimento compartilhado aqui visa contribuir para a ciência e a preservação do meio ambiente.

---

## 📦 Releases

Para obter as versões mais recentes e baixar os arquivos necessários, visite a seção de [Releases](https://github.com/Itazimkhan/ufrj-sensoriamento-remoto/releases). Siga as instruções específicas para cada versão.

---

## 📞 Contato

Para mais informações ou dúvidas, entre em contato através do e-mail: contato@ufrj-sensoriamento-remoto.com.

---

## 📸 Imagens

![Imagem de Satélite](https://example.com/imagem-satelite.jpg)
*Exemplo de imagem de satélite utilizada nas análises.*

![Gráfico de Análise](https://example.com/grafico-analise.jpg)
*Gráfico demonstrando os resultados da análise de dados.*

---

## 🌐 Links Úteis

- [Google Earth Engine](https://earthengine.google.com/)
- [Documentação do Pandas](https://pandas.pydata.org/pandas-docs/stable/)
- [Documentação do Matplotlib](https://matplotlib.org/stable/contents.html)

---

Explore, analise e contribua para o avanço do conhecimento em Sensoriamento Remoto!
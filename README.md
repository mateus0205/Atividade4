

# Previsão de Casos de Autismo em Adultos Usando Base de Dados AIQ-10

Este projeto utiliza um modelo de machine learning para prever a probabilidade de um diagnóstico de autismo em adultos com base em dados coletados pelo questionário AIQ-10 (Autism Spectrum Quotient, 10 questões). A base de dados contém respostas a perguntas sobre comportamento e características pessoais que auxiliam na identificação de possíveis sinais de autismo.

## Objetivo

O objetivo deste projeto é treinar e testar um modelo de previsão que, a partir das respostas do AIQ-10, pode indicar se um adulto possui ou não um diagnóstico potencial de autismo. Essa previsão é útil para auxiliar profissionais da saúde na triagem inicial de casos suspeitos.

## Estrutura do Projeto

1. **Data Preparation**: A base de dados é carregada e os dados são pré-processados para uso no modelo. Este passo inclui:
   - Limpeza dos dados (remoção de valores nulos ou inconsistentes).
   - Codificação de variáveis categóricas.
   - Divisão entre dados de treino e teste.

2. **Modelagem**: Um modelo de machine learning, como uma Regressão Logística ou uma árvore de decisão, é treinado usando os dados de treino.

3. **Avaliação**: O modelo é avaliado usando métricas de performance (como acurácia, precisão, recall, e F1-score) nos dados de teste, permitindo análise da eficácia do modelo.

4. **Previsão**: Após a avaliação, o modelo é utilizado para fazer previsões com base nas respostas do questionário AIQ-10.
Esses resultados da matriz de confusão e das métricas de desempenho do modelo devem ser incluídos na seção de **Avaliação** do README. Essa seção já menciona a avaliação do modelo com métricas, então você pode expandi-la para detalhar os resultados específicos que o modelo obteve no conjunto de teste. 


## Avaliação

O modelo foi testado em um conjunto de dados de validação para medir sua precisão e capacidade de prever corretamente casos de autismo. A matriz de confusão a seguir mostra os resultados de desempenho:

|                | Predito Não-Autista (0) | Predito Autista (1) |
|----------------|-------------------------|----------------------|
| **Verdadeiro Não-Autista (0)** | 105                     | 0                    |
| **Verdadeiro Autista (1)**     | 0                       | 36                   |

Esses resultados indicam que o modelo teve uma **acurácia perfeita** (100%) nos dados de teste, com as seguintes métricas:

- **Acurácia**: 100%
- **Precisão para classe Autista (1)**: 100%
- **Recall para classe Autista (1)**: 100%
- **Precisão para classe Não-Autista (0)**: 100%
- **Recall para classe Não-Autista (0)**: 100%

A ausência de erros de classificação sugere que o modelo foi muito bem-sucedido na separação dos casos de autismo e não-autismo para este conjunto de dados. No entanto, é importante testar o modelo em outros conjuntos de dados para garantir que ele mantenha esse desempenho com novos dados.

## Pré-requisitos

Para rodar o código, você precisará de:

- Python 3.6 ou superior
- Pandas
- NumPy
- Scikit-learn
- Matplotlib (para visualizações)

Esses pacotes podem ser instalados com o seguinte comando:

```bash
pip install pandas numpy scikit-learn matplotlib
```

## Como Rodar

1. Clone este repositório e navegue até o diretório principal do projeto.

2. Carregue o conjunto de dados `aiq_10_autism.csv` (ou outro nome de base de dados usada no projeto) na pasta de dados ou atualize o caminho da base de dados no código.

3. Execute o script principal:

   ```bash
   python main.py
   ```

4. O script exibirá as métricas de avaliação do modelo e, dependendo do código, poderá gerar gráficos ou relatórios com os resultados.

## Estrutura dos Dados

O conjunto de dados AIQ-10 inclui colunas como:

- **Question 1 to 10**: Respostas para as 10 perguntas do questionário (valores numéricos ou categóricos).
- **Age**: Idade do respondente.
- **Gender**: Gênero do respondente.
- **Ethnicity**: Etnia do respondente.
- **Jaundice**: Histórico de icterícia infantil.
- **Family ASD**: Histórico de autismo na família.
- **Class/Label**: Rótulo indicando se o respondente foi diagnosticado com autismo.

## Exemplo de Uso

Com o modelo treinado, você pode realizar previsões diretamente sobre novas respostas ao questionário AIQ-10. Um exemplo de código para prever um novo caso está incluído no script `predict.py`.

## Contribuindo

Contribuições para melhorar a precisão do modelo e a usabilidade do código são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests com sugestões ou correções.

## Licença

Este projeto é distribuído sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes.

---
## 🤝 Colaboradores

Agradecemos às seguintes pessoas que contribuíram para este projeto:

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/lucaspvc">
        <img width=100 src="https://avatars.githubusercontent.com/u/117240748?v=4" width="100px;" alt="Foto do Lucas Pessoa no gitHub"/><br>
        <sub>
          <b>Lucas Pessoa</b>
        </sub>
      </a>
    </td>
    <td align="center">
          <a href="https://github.com/mateus0205">
            <img width=100 src="https://avatars.githubusercontent.com/u/89797706?v=4" width="100px;" alt="Foto do Steve Jobs"/><br>
            <sub>
              <b>Mateus Martins </b>
            </sub>
          </a>
     </td>
  </tr>
</table>

---

Esse README pode ser ajustado conforme necessário, dependendo dos detalhes específicos do seu código e da estrutura de dados.

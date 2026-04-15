# NLW Operator - LeNet-5 MNIST Classification

Este projeto consiste na implementação e treinamento da arquitetura clássica de rede neural **LeNet-5** para o reconhecimento de dígitos manuscritos, utilizando o dataset **MNIST** e o framework **PyTorch**.

## 🚀 Estrutura do Projeto

*   `lenet5.ipynb`: Notebook principal com todo o fluxo de desenvolvimento:
    *   Definição da arquitetura LeNet-5.
    *   Visualização de filtros convolucionais.
    *   Processamento e visualização do dataset MNIST.
    *   Loop de treinamento e otimização.
    *   Avaliação de performance e métricas de acurácia.
    *   Análise de erros (Galeria do Fracasso).
    *   Visualização de Feature Maps (Ativações internas).
*   `minha_lenet5_mnist.pth`: Pesos do modelo já treinados e prontos para uso.
*   `main.py`: Script base do projeto.
*   `pyproject.toml`: Configurações de dependências e ambiente (utilizando `uv`).

## 🛠️ Tecnologias Utilizadas

*   **Python 3.11+**
*   **PyTorch**: Framework principal para Deep Learning.
*   **Torchvision**: Utilizado para carregar e transformar o dataset MNIST.
*   **Matplotlib**: Utilizado para todas as visualizações (filtros, dados, gráficos).
*   **UV**: Gerenciador de pacotes e ambientes Python de alto desempenho.

## 📈 Resultados

O modelo foi treinado por 5 épocas, atingindo uma alta precisão no conjunto de teste. O projeto inclui uma seção de "Galeria do Fracasso", onde é possível inspecionar visualmente os dígitos que a rede teve dificuldade em classificar, além de Feature Maps que mostram como os 6 filtros da primeira camada abstraem bordas e formas.

## 💻 Como Executar

1.  Certifique-se de ter o `uv` instalado.
2.  Instale as dependências:
    ```bash
    uv sync
    ```
3.  Abra o notebook `lenet5.ipynb` e execute as células para treinar ou carregar o modelo.

## 🧠 Carregando o Modelo Treinado

Para utilizar o modelo salvo em suas próprias aplicações:

```python
import torch
from lenet5 import LeNet5 # Certifique-se de ter a classe definida

modelo = LeNet5(num_classes=10)
modelo.load_state_dict(torch.load('minha_lenet5_mnist.pth'))
modelo.eval()
```

---
Projeto desenvolvido como parte do aprendizado em Deep Learning e Visão Computacional.

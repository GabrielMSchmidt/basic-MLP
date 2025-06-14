# MLP Básica para Classificação de Estrelas Pulsares

Este repositório apresenta a construção de uma rede neural **Multi-Layer Perceptron (MLP)** a partir do zero, utilizando apenas a biblioteca **NumPy** para todas as operações de álgebra linear e o processo de treinamento. O objetivo é classificar possíveis estrelas pulsares.

Este projeto foi desenvolvido como um exercício prático para aprofundar o entendimento sobre os mecanismos fundamentais de uma rede neural, sem a abstração de frameworks como TensorFlow ou PyTorch.

Ele foi feito durante a disciplina de Computação Natural por mim e 2 colegas de classe.



---

## 🧠 Funcionamento da Rede Neural

A implementação cobre todas as etapas essenciais do funcionamento de uma MLP:

1.  **Estrutura da Rede**: A arquitetura da rede é definida com uma camada de entrada, uma camada oculta e uma camada de saída. Os pesos e biases são inicializados aleatoriamente.

2.  **Forward Propagation (Etapa de Predição)**:
    * Os dados de entrada (possíveis estrelas) são "achatados" (flattened) em um vetor.
    * A entrada é multiplicada pelos pesos da primeira camada, e o bias é somado.
    * A função de ativação **Tangente Hiperbólica** é aplicada ao resultado.
    * O processo se repete para a camada de saída, que utiliza a **função Sigmóide** para converter os scores em probabilidades para uma das duas classes.

3.  **Backpropagation e Otimização (Etapa de Treinamento)**:
    * O erro entre a predição (saída da Sigmóide) e o rótulo verdadeiro é calculado usando a função de perda **Binary Cross Entropy**.
    * O algoritmo de **backpropagation** é implementado para calcular o gradiente da função de perda em relação a cada peso e bias da rede.
    * Os pesos e biases são atualizados na direção oposta ao gradiente, aplicando o algoritmo de otimização **Gradiente Descendente**, com uma taxa de aprendizado (`learning rate`) definida.

O ciclo de *forward propagation*, cálculo do erro e *backpropagation* é repetido por várias épocas (iterações sobre todo o conjunto de dados de treino) para minimizar o erro e "ensinar" a rede a classificar os dígitos corretamente.

---

## 📊 Resultados de Desempenho

A performance do modelo foi avaliada no conjunto de teste do dataset. Os resultados obtidos foram os seguintes:

| Métrica         | Valor |
| :-------------- | :---: |
| Acurácia        |   97%  |
| Precisão (Média) |   94% |
| Recall (Média)   |   69% |
| F1-Score (Média) |   80% |

---

## Autores

- [@GabrielMSchmidt](https://www.github.com/GabrielMSchmidt)
- [@GabrielNLima](https://www.github.com/GabrielNLima)
- [@KWSantos](https://www.github.com/KWSantos)


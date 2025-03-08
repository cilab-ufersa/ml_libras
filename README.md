# ML LIBRAS
Machine learning approaches for efficient recognition of Brazilian Sign Language

## 1. Organização 

- `data/`: arquivos csv com os dados utilizados no projeto.
- `model/`: arquivo pkl com o modelo treinado.

## 2. Dados

Dentro da pasta de `data/` temos os seguint arquivos:

- `44_classes_dataset.csv`: dataset com 44 classes de sinais da LIBRAS.
- `balanced_train_dataset.csv`: dataset balanceado para treinamento.
- `input_train_dataset.csv`: dataset (desbalanceado) para treinamento do modelo.	
- `input_validation_dataset.csv`: dataset para validação do modelo.
- `pycaret_25_classes_results.csv`: resultados dos modelos de classificação para 25 classes.
- `pycaret_44_classes_results.csv`: resultados dos modelos de classificação para 44 classes.
- `test_dataset.csv`: dataset para teste do modelo.

## 3. Modelo

A pasta `model/` contém o modelo Extra Trees treinado com o dataset `balanced_train_dataset.csv`. As métricas do modelo são apresentadas abaixo.

| Modelo | Acurácia | AUC | Recall | Precisão | F1 | Tempo de treinamento (s) | Tempo de inferência (s)| 
| --- | --- | --- | --- | --- | --- | --- | --- |
| Extra Trees | 0.9801 | 0.9995 | 0.9801 | 0.9802 | 0.9801 | 12.4980 | 0.002730|

O modelo recebe como entrada um vetor de 126 itens. Onde os 63 primeiros itens representam as coordenadas x, y e z da mão direita e os 63 últimos itens representam as coordenadas da mão esquerda.


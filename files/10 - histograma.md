**Python - Gráficos, Visualizações e Dashboards** 
>**histogramas**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Histograma

Importação das bibliotecas:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

Carregamento da base de dados:

```python
base = pd.read_csv('trees.csv')
base.shape
```

Resultado:

```
(31, 3)
```

Dados:

```python
base.head()
```

![Alt text](/assets/10-1.png)

Criação do histograma, considerando somente o segundo atributo da base de dados e com duas divisões (bins):

```python
h = np.histogram(base.iloc[:,1], bins = 6)
```

Resultado:

```
(array([4, 2, 5, 7, 9, 4], dtype=int64),
 array([63., 67., 71., 75., 79., 83., 87.]))
```

Visualização do histograma com 6 divisões (bins):

```python
plt.hist(base.iloc[:,1], bins = 6)
plt.title('Árvores')
plt.ylabel('Frequência')
plt.xlabel('Altura')
```

Resultado (gráfico):

![Árvores](/assets/10-2.png)



&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
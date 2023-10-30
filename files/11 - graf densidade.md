**Python - Gráficos, Visualizações e Dashboards** 
>**Gráficos de Densidade**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Gráficos de Densidade

#### Importação das bibliotecas
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

#### Carregamento da base de dados
```python
base = pd.read_csv('trees.csv')
base.head()
```

![Alt text](/assets/11-1.png)

#### Histograma com 10 divisões (bins) e somente para o primeiro atributo da base de dados
```python
plt.hist(base.iloc[:,1], bins = 6)
```

![Alt text](/assets/11-2.png)

#### Histograma com a linha de distribuição de frequência, com 6 divisões (bins)
*kde = linha de densidade*
```python
sns.histplot(base.iloc[:,1], kde=False, bins=6, color='blue').set(title='Árvores')
```

![Alt text](/assets/11-3.png)

#### Densidade, método kdeplot para densidade
```python
sns.kdeplot(base.iloc[:,1], color='blue').set(title='Árvores')
```

![Alt text](/assets/11-4.png)

#### Densidade e histograma
```python
sns.histplot(base.iloc[:,1], kde=True, bins=6, color='blue').set(title='Árvores')
```

![Alt text](/assets/11-5.png)



&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
**Python - Gráficos, Visualizações e Dashboards** 
>**Histograma com densidade e seabord**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



## Histograma com Densidade e Seaborn

#### Importação das bibliotecas
```python
import pandas as pd
import seaborn as srn
import matplotlib.pyplot as plt
```

#### Carregamento da base de dados (trees.csv)
```python
base = pd.read_csv('trees.csv')
base.head()
```

![Alt text](/assets/19-1.png)

#### Histograma com 10 divisões (bins) e com gráfico de densidade (kernel density - suavização)
*stat: count, frequency, probability, percent, density*
```python
srn.histplot(base.Volume, color="blue", kde=True, stat="density", bins=10).set(title='Volume')
```

![Alt text](/assets/19-2.png)

#### Carregamento de outra base de dados (chicken.csv)
```python
base2 = pd.read_csv('chicken.csv')
base2.head()
```

![Alt text](/assets/19-3.png)

#### Criação de um novo dataframe agrupando o atributo 'feed'
```python
agrupado = base2.groupby(['feed'])['weight'].sum()
agrupado
```

![Alt text](/assets/19-4.png)

#### Novo dataframe somente para testar os filtros do pandas
```python
teste = base2.loc[base2['feed'] == 'horsebean']
teste
```

![Alt text](/assets/19-5.png)

#### Histograma considerando somente o valor 'horsebean'
*Apenas o gráfico de densidade neste caso*
```python
srn.kdeplot(base2.loc[base2['feed'] == 'horsebean'].weight).set(title='horsebean')
```

![Alt text](/assets/19-6.png)

#### Histograma considerando somente o valor 'casein'
```python
srn.histplot(base2.loc[base2['feed'] == 'casein'].weight, kde=True).set(title='casein')
```

![Alt text](/assets/19-7.png)

#### Histograma considerando somente o valor 'linseed'
```python
srn.histplot(base2.loc[base2['feed'] == 'linseed'].weight, kde=True).set(title='linseed')
```

![Alt text](/assets/19-8.png)

#### Histograma considerando somente o valor 'meatmeal'
```python
srn.histplot(base2.loc[base2['feed'] == 'meatmeal'].weight, kde=True).set(title='meatmeal')
```

![Alt text](/assets/19-9.png)

#### Histograma considerando somente o valor 'soybean'
```python
srn.histplot(data=base2.loc[base2['feed'] == 'soybean'].weight, kde=True).set(title='soybean')
```

![Alt text](/assets/19-10.png)

#### Histograma considerando somente o valor 'sunflower'
```python
srn.histplot(base2.loc[base2['feed'] == 'sunflower'].weight, kde=True).set(title='sunflower')
```

![Alt text](/assets/19-11.png)

#### Impressão em um gráfico 2 x 3 (3 linhas 2 colunas)
```python
plt.figure()
plt.subplot(3,2,1)
srn.histplot(base2.loc[base2['feed'] == 'horsebean'].weight, kde=True).set(title='horsebean')
plt.subplot(3,2,2)
srn.histplot(base2.loc[base2['feed'] == 'casein'].weight, kde=True).set(title='casein')
plt.subplot(3,2,3)
srn.histplot(base2.loc[base2['feed'] == 'linseed'].weight, kde=True).set(title='linseed')
plt.subplot(3,2,4)
srn.histplot(base2.loc[base2['feed'] == 'meatmeal'].weight, kde=True).set(title='meatmeal')
plt.subplot(3,2,5)
srn.histplot(base2.loc[base2['feed'] == 'soybean'].weight, kde=True).set(title='soybean')
plt.subplot(3,2,6)
srn.histplot(base2.loc[base2['feed'] == 'sunflower'].weight, kde=True).set(title='sunflower')
#ajusta o layout para não haver sobreposição
plt.tight_layout()
```

![Alt text](/assets/19-12.png)

&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
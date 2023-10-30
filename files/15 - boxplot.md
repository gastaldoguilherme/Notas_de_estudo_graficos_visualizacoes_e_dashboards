**Python - Gráficos, Visualizações e Dashboards** 
>**Boxplot**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;

## Boxplot



#### Importação das bibliotecas
```python
import pandas as pd
import matplotlib.pyplot as plt
```

#### Carregamento da base de dados
```python
base = pd.read_csv('trees.csv')
base.head()
```

![Alt text](/assets/15-1.png)

#### Geração do boxplot para o atributo "Volume"
*patch_artist = True preenche, showfliers mostra os outliers*
```python
plt.boxplot(base.Volume, vert=False, showfliers=False, notch=True, patch_artist=True)
plt.title('Árvores')
plt.xlabel('Volume')
```

![Alt text](/assets/15-2.png)

#### Boxplot para todos os atributos na base de dados
```python
plt.boxplot(base)
plt.title('Árvores')
plt.xlabel('Dados')
```

![Alt text](/assets/15-3.png)

#### Geração de 3 Boxplots individuais para os atributos "Volume," "Girth," e "Height"
```python
plt.boxplot(base.Volume, vert=False)
plt.boxplot(base.Girth, vert=False)
plt.boxplot(base.Height, vert=False)
plt.title('Árvores')
plt.xlabel('Dados')
```

![Alt text](/assets/15-4.png)



&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
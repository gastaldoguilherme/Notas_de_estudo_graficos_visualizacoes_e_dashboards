**Python - Gráficos, Visualizações e Dashboards** 
>**Gráfico de dispersão**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Gráfico de Dispersão

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

![Alt text](/assets/12-1.png)

#### Gráfico de dispersão considerando o volume e a circunferência
```python
plt.scatter(x=base.Girth, y=base.Volume, color='blue', facecolors='none', marker='*')
plt.title('Árvores')
plt.xlabel('Circunferência')
plt.ylabel('Volume')
```

![Alt text](/assets/12-2.png)

#### Gráfico de linha considerando o volume e o atributo "girth" - sem marker
```python
plt.plot(base.Girth, base.Volume)
plt.title('Árvores')
plt.xlabel('Circunferência')
plt.ylabel('Volume')
```

![Alt text](/assets/12-3.png)

#### Gráfico de dispersão com 'afastamento' dos dados (jitter)
*fit_reg linha de tendência*
```python
sns.regplot(x=base.Girth, y=base.Volume, data=base, x_jitter=0.3, fit_reg=False)
```

![Alt text](/assets/12-4.png)




&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
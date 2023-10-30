**Python - Gráficos, Visualizações e Dashboards** 
>**Boxplot com Seaborn**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


### Boxplot com Seaborn

#### Importação das bibliotecas
```python
import pandas as pd
import seaborn as sns
```

#### Carregamento da base de dados
```python
base = pd.read_csv('trees.csv')
base.head()
```

![Alt text](/assets/18-1.png)

#### Visualização de um boxplot para o atributo "Volume"
```python
sns.boxplot(data=base.Volume, orient='v').set_title('Árvores')
```

![Alt text](/assets/18-2.png)

#### Visualização de vários boxplots na mesma imagem
```python
sns.boxplot(data=base)
```

![Alt text](/assets/18-3.png)





&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
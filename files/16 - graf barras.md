**Python - Gráficos, Visualizações e Dashboards** 
>**Gráfico de Barras**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;



## Gráfico de Barras

#### Importação do pandas para leitura de arquivos .csv
```python
import pandas as pd
```

#### Carregamento da base de dados (insect.csv)
```python
base = pd.read_csv('insect.csv')
base.shape
```

Resultado:

```
(72, 2)
```

#### Dados da base
```python
base.head()
```

![Alt text](/assets/16-1.png)

#### Agrupamento dos dados baseado no atributo 'spray', contagem e soma dos registros
```python
agrupado = base.groupby(['spray'])['count'].sum()
agrupado
```

![Alt text](/assets/16-2.png)

#### Gráfico de barras
```python
agrupado.plot.bar(color='gray')
```

![Alt text](/assets/16-3.png)

#### Gráfico de barras com cores personalizadas
```python
agrupado.plot.bar(color=['blue', 'yellow', 'red', 'green', 'pink', 'orange'])
```

![Alt text](/assets/16-4.png)





&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
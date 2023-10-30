**Python - Gráficos, Visualizações e Dashboards** 
>**Gráfico de Pizza**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


## Gráfico de Pizza

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

![Alt text](/assets/17-1.png)

#### Gráfico de pizza
```python
agrupado.plot.pie()
```

![Alt text](/assets/17-2.png)

#### Gráfico de pizza com legenda
```python
agrupado.plot.pie(legend=True)
```

![Alt text](/assets/17-3.png)



&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
**Python - Gráficos, Visualizações e Dashboards** 
>**Divisão da tela (subgráficos)**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


### Divisão da Tela (Subgráficos)

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

![Alt text](/assets/14-1.png)

#### Gráfico de dispersão: girth com volume
```python
plt.scatter(base.Girth, base.Volume)
```

![Alt text](/assets/14-2.png)

#### Gráfico de dispersão: height com volume
```python
plt.scatter(base.Height, base.Volume, marker='*')
```

![Alt text](/assets/14-3.png)

#### Histograma de volume
```python
plt.hist(base.Volume)
```

![Alt text](/assets/14-4.png)

#### Imprimindo os gráficos juntos em subgráficos
```python
# Criação de uma figura na qual os gráficos serão posicionados
plt.figure(1)
plt.subplot(2, 2, 1)
plt.scatter(base.Girth, base.Volume)
plt.subplot(2, 2, 2)
plt.scatter(base.Girth, base.Height)
plt.subplot(2, 2, 3)
plt.scatter(base.Height, base.Volume, marker='*')
plt.subplot(2, 2, 4)
plt.hist(base.Volume)
```

![Alt text](/assets/14-5.png)



&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
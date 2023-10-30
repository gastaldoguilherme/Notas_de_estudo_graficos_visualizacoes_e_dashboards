**Python - Gráficos, Visualizações e Dashboards** 
>**Gráfico de dispersão com legenda**    
> Repositório: python - Fundamentos  
> GitHub: @gastaldoguilherme
&nbsp;


### Gráfico de Dispersão com Legenda

#### Importação das bibliotecas
```python
import pandas as pd
import matplotlib.pyplot as plt
```

#### Carregamento da base de dados
```python
base = pd.read_csv('co2.csv')
base.head()
```

![Alt text](/assets/13-1.png)

#### Criando duas variáveis para cada atributo (x = conc e y = uptake)
```python
x = base.conc
y = base.uptake
```

#### Retorna os valores únicos do atributo "treatment"
```python
unicos = list(set(base.Treatment))
unicos
```

Resultado:

```
['nonchilled', 'chilled']
```

#### Percorre cada tipo de tratamento (chilled e nonchilled) e cria um gráfico de dispersão com legenda
```python
for i in range(len(unicos)):
    indice = base.Treatment == unicos[i]
    plt.scatter(x[indice], y[indice], label=unicos[i])
plt.legend(loc='lower right')
```

![Alt text](/assets/13-2.png)


&nbsp;

<div align="center">
   
[Retornar ao índice](/README.md)

</div>
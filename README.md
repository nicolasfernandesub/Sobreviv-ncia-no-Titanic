# Sobreviv-ncia-no-Titanic
# Primeiro projeto Na Área de dados

import pandas as pd

# Criando base de dados 
dados= {'Passageiro':[1,2,3], 'Sexo': ['male','female','female'], 'Idade':[22,None,38]}
df_titanic = pd.DataFrame(dados)


#preenchendo as idades vazias com a média e  convertendo a coluna de texto para números
df_titanic['Idade'] = df_titanic['Idade'].fillna(df_titanic['Idade'].mean())
df_titanic['Sexo'] = df_titanic['Sexo'].map({'male':0,'feale':1})

print(df_titanic)

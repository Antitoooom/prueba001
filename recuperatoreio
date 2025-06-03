Obvtener el nombre de todos los usuarios mayores a 30 años de los paises Francia Alemania y España 
Obvtener todos los usuarios entre las edades de 45 6y 50 
Con graficos. 


import pandas as pd
import matplotlib.pyplot as plt

# Leer el archivo CSV
df = pd.read_csv("users.csv")


filtro1 = (df['edad'] > 30) & (df['pais'].isin(['France', 'Germany', 'Spain']))
usuarios_mayores_30 = df[filtro1]


conteo_por_pais = usuarios_mayores_30['pais'].value_counts()


plt.figure(figsize=(8,5))
conteo_por_pais.plot(kind='bar', color='skyblue')
plt.title('Usuarios mayores de 30 por país (Francia, Alemania, España)')
plt.xlabel('País')
plt.ylabel('Cantidad de usuarios')
plt.tight_layout()
plt.show()


filtro2 = (df['edad'] >= 45) & (df['edad'] <= 50)
usuarios_45_50 = df[filtro2]

conteo_45_50 = usuarios_45_50['pais'].value_counts()


plt.figure(figsize=(6,6))
conteo_45_50.plot(kind='pie', autopct='%1.1f%%', startangle=90)
plt.title('Distribución de usuarios entre 45 y 50 años por país')
plt.ylabel('')
plt.tight_layout()
plt.show()

import pandas as pd

# Cargar los datos desde las URLs
url_t1 = "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_1%20.csv"
url_t2 = "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_2.csv"
url_t3 = "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_3.csv"
url_t4 = "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science-latam/refs/heads/main/base-de-datos-challenge1-latam/tienda_4.csv"

# Leer los datos de las tiendas
tienda_1 = pd.read_csv(url_t1)
tienda_2 = pd.read_csv(url_t2)
tienda_3 = pd.read_csv(url_t3)
tienda_4 = pd.read_csv(url_t4)

# Función para calcular las métricas clave de cada tienda
def analizar_tienda(dataframe):
    ingresos_totales = dataframe["Precio"].sum()
    costos_envios_totales = dataframe["Costo de envío"].sum()
    calificacion_promedio = dataframe["Calificación"].mean()
    return ingresos_totales, costos_envios_totales, calificacion_promedio

# Análisis de cada tienda
ingresos_1, envios_1, calificacion_1 = analizar_tienda(tienda_1)
ingresos_2, envios_2, calificacion_2 = analizar_tienda(tienda_2)
ingresos_3, envios_3, calificacion_3 = analizar_tienda(tienda_3)
ingresos_4, envios_4, calificacion_4 = analizar_tienda(tienda_4)

# Mostrar los resultados de análisis por tienda
print("Resultados del análisis por tienda:")
print(f"Tienda 1: Ingresos: {ingresos_1}, Costo de envíos: {envios_1}, Calificación promedio: {calificacion_1}")
print(f"Tienda 2: Ingresos: {ingresos_2}, Costo de envíos: {envios_2}, Calificación promedio: {calificacion_2}")
print(f"Tienda 3: Ingresos: {ingresos_3}, Costo de envíos: {envios_3}, Calificación promedio: {calificacion_3}")
print(f"Tienda 4: Ingresos: {ingresos_4}, Costo de envíos: {envios_4}, Calificación promedio: {calificacion_4}")

# Tomar la decisión de cierre
decision = "Cerrar la tienda 1 debido a menor desempeño financiero, altos costos de envío y calificaciones bajas."
print("Decisión final:", decision) la desicion se tomó en base a lay de concursos y qiebras argentina pese a qué esto es Colombia y cada país tiene su ley de concursos y quiebras  el programa analizado detecta que la tienda uno tiene la mayor perdida 

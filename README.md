
![image](https://github.com/Grupo-16-ISPC/proyecto_alquileres/assets/107323698/4acbff54-c327-40a7-b9d5-531e4ab72b4f)

# Grupo 16 ISPC – TCDIA

![image](https://github.com/Grupo-16-ISPC/proyecto_alquileres/assets/107323698/2395ddd9-b4bd-4002-8803-cf05f0862597)



# Proyecto Análisis de Alquileres

 


## Integrantes:
### Ancillotti Angel, Científico de Datos.
### Juan Zorrilla, Arquitecto.
### Pablo Mercado, Sociólogo.
### Ibarra Facundo, Ingeniero de Datos





# Resumen Ejecutivo:

Este informe aborda el análisis de alquileres en relación a la predicción de precios en el mercado inmobiliario de Argentina, con el objetivo de proporcionar una herramienta eficaz para la toma de decisiones informadas en el sector. El proyecto se enmarca en siete ejes estratégicos: obtención y almacenamiento de datos, Data Cleaning Exploración y visualización, Análisis descriptivo, Feature Engieneering, Modelos de Aprendizaje, métricas de Evaluación, Evaluación del modelo Final. La combinación de estos elementos ofrece una base sólida, tanto teórica como práctica, para impulsar la transparencia y eficiencia en el mercado inmobiliario argentino.
Este análisis, esta centrado en el análisis de datos mediante técnicas de Web Scraping para la obtención de datos, Técnicas EDA y ETL para obtener un DataFrame preciso para el armado del Modelo de Machine Learning.  Con el modelo definido, aplicamos diferentes métricas para su evaluación, rendimiento y un posterior ajuste para optimizar el modelo. 





# Scraping y Análisis de Alquileres del portal argenprop.com
### Descripción:
----


### Archivos:
El archivo scrap_2 cuenta con tres funciones distintas, y una cuarta que se encarga de orquestarlas (main()):
* **obtener_enlaces_desde_inicio():** Obtiene una lista de enlaces de la página principal de Argenprop que corresponden a categorías específicas de propiedades de alquiler y barrios de CABA.
  * Retorna: Lista de enlaces que corresponden a las categorías deseadas.
* **obtener_todos_enlaces_de_pagina(pagina_url):** Recopila todos los enlaces de propiedades individuales en una página de categoría dada.
  * Parámetros: pagina_url (str): URL de la página de la categoría de la que se quieren obtener los enlaces.
  * Retorna: Lista de enlaces a listados individuales de propiedades.
* **extraer_datos_de_enlace(enlace):** Extrae detalles específicos de una página de listado de propiedad individual.
  * Parámetros: enlace (str): Enlace a la página de listado de propiedad individual.
  * Retorna: Un diccionario que contiene información sobre la propiedad. Si ocurre un error o no se puede obtener la información, se devuelve None.
* **main():** Función principal que coordina la ejecución de las demás funciones, recolecta datos y guarda la información en un archivo CSV.
  * Retorna: Se crea un archivo CSV llamado propiedades_argenprop.csv con los datos recolectados. 

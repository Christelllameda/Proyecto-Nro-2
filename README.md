<div align="center">

# **Proyecto Nro 2 - Building mySQL Data-base** </div>
![Proyecto Nro 2 - Building mySQL Data-base](https://i.postimg.cc/JnxfCpBM/image-87.webp)


---
</div>

# Introducción
Este proyecto tiene como objetivo principal la creación de una base de datos utilizando SQL (Structured Query Language). 

La base de datos servirá como un almacén centralizado de información, permitiendo el acceso, búsqueda y análisis de datos de manera eficaz. 

Este proyecto abordará la definición de tablas, relaciones, índices y consultas SQL que cumplirán con las necesidades específicas de la organización. La creación de esta base de datos contribuirá a la toma de decisiones informadas y mejorará la eficiencia de la organización en la gestión de sus activos de datos."

# Contenido
- [data](https://github.com/Christelllameda/Proyecto-Nro-2/tree/main/data)
    - [cvs_originales](https://github.com/Christelllameda/Proyecto-Nro-2/tree/main/data/csv_originales)
    - [cvs_limpios](https://github.com/Christelllameda/Proyecto-Nro-2/tree/main/data/csv_limpios)
- [src](https://github.com/Christelllameda/Proyecto-Nro-2/tree/main/src)
    - [jupyter](https://github.com/Christelllameda/Proyecto-Nro-2/tree/main/src/jupyter)
        - [Limpieza de datos](https://github.com/Christelllameda/Proyecto-Nro-2/tree/main/src/jupyter/Limpieza%20de%20datos)
        - [Creación base de datos](https://github.com/Christelllameda/Proyecto-Nro-2/blob/main/src/jupyter/Base%20de%20datos.ipynb)
- [imagen](https://github.com/Christelllameda/Proyecto-Nro-2/tree/main/imagen)


# Objetivos
El objetivo principal de la creación de esta base de datos y su posterior análisis, es demostrar si es rentable reabrir un videoclub. Para ello necesitaremos:

Determinar el día que mas se alquilan películas.

Definir cuál es la categoría de películas que mas se suelen alquilar.

Determinar el total de dinero obtenido por rentas de películas en un día.

# Exploración de datos


# Conclusión

SELECT o.category,SUM(f.rental_rate) AS max_rental_rate
FROM film f
JOIN old_hdd o ON f.title = o.title
JOIN rental r ON f.rental_duration = r.rental_duration
GROUP BY o.category
ORDER BY max_rental_rate DESC;
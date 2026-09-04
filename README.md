## Dashboard_Andes_Capital_Real_Estate
Dashboard interactivo para entender el desempeño comercial de los años 2024–2025 de Andes Capital Real Estate


## Proyecto 10: Dashboard de análisis comercial inmobiliario
Como analista de datos en una empresa inmobiliaria se necesita comprender mejor el desempeño comercial. La empresa gestiona la venta de diferentes tipos de propiedades a través de distintos canales de venta y segmentos de clientes. Actualmente, la información existe a nivel transaccional, pero no hay una visión analítica clara del negocio.



# Objetivo del proyecto
Construir un dashboard interactivo en Power BI o Tableau que permita analizar ventas, clientes y propiedades para apoyar decisiones estratégicas. El dashboard debe ayudar a responder preguntas como:

¿Cuál es el ingreso total generado por las ventas de propiedades?
¿Qué tipo de propiedad genera más ingresos?
¿Qué segmentos de clientes compran más?
¿Cómo evolucionan las ventas en el tiempo?
¿El negocio está creciendo año contra año?
¿Los clientes vuelven a comprar después de su primera compra?

Con ello se logró:
- Preparar y validar datos para análisis.
- Construir un modelo de datos en esquema estrella.
- Crear medidas analíticas para análisis comercial.
- Aplicar inteligencia de tiempo para analizar tendencias.
- Diseñar dashboards claros para análisis ejecutivo.
- Analizar la recurrencia de clientes utilizando cohortes.


# El dataset contiene las siguientes columnas:

El proyecto utiliza una tabla de hechos (ventas) y tablas dimensionales (clientes y propiedades).

- hecho_ventas_propiedades: Cada fila representa la transacción de venta de una propiedad. Este dataset permitirá analizar ventas, comisiones, canales comerciales y tendencias en el tiempo.

id_venta	| Categórica	| Identificador único de la venta	| SALE000001
fecha_venta	| Fecha	| Fecha en que se realizó la venta	| 2024-01-05
id_cliente	| Categórica	| Identificador del cliente que realizó la compra	| CUST02497
id_propiedad	| Categórica	| Identificador de la propiedad vendida	| PROP03591
ciudad	| Categórica	| Ciudad donde se realizó la venta	| Bogotá
precio_venta	| Numérico (decimal)	| Precio final de venta de la propiedad	| 1027126
tipo_propiedad	| Categórica	| Tipo de propiedad vendida	| Casa
canal_venta	| Categórica	| Canal utilizado para la venta	| Corredor
porcentaje_comision	| Numérico (decimal)	| Porcentaje de comisión aplicado en la venta	| 0.0473
monto_comision	| Numérico (decimal)	| Monto de comisión generado por la venta	| 48605


- dim_clientes : Cada fila representa un cliente. Este dataset permitirá analizar la segmentación de clientes y el comportamiento de compra por ubicación o tipo de comprador.

id_cliente	| Categórica	| Identificador único del cliente	| CUST00001
segmento_comprador	| Categórica	| Tipo o perfil del comprador	| Primera vez
pais	| Categórica	| País del cliente	| Colombia
ciudad	| Categórica	| Ciudad del cliente	| Bogotá


- dim_propiedades: Cada fila representa una propiedad disponible para venta. Este dataset permitirá analizar características de las propiedades y su relación con el desempeño comercial.

id_propiedad	| Categórica	| Identificador único de la propiedad	| PROP00001
tipo_propiedad	| Categórica	| Tipo de propiedad	| Departamento
ciudad	| Categórica	| Ciudad donde se ubica la propiedad	| Bogotá
barrio	| Categórica	| Barrio o zona de la propiedad	| Usaquén
habitaciones	| Numérico (int) |	Número de habitaciones	| 2
tamano_m2	| Numérico (int)	| Tamaño de la propiedad en metros cuadrados |	79
precio_publicado	| Numérico (decimal)	| Precio inicial publicado de la propiedad	| 322670
categoria_propiedad	| Categórica	| Categoría de la propiedad	| Residencial


- dim_fecha: Durante el proyecto se creó una tabla calendario llamada dim_fecha que permitió realizar análisis temporal como: Tendencias de ventas, Comparaciones Year over Year, Métricas acumuladas YTD y MTD. Incluye campos como:

Date	| Fecha	| Fecha del calendario	| 2024-01-05
Año	| Numérico (int)	| Año de la fecha	| 2024
Mes	| Categórica	| Nombre del mes	| Enero
Mes Numero	| Numérico (int)	| Número del mes |	1
Año-Mes	| Categórica	| Año y mes en formato analítico	| 2024-01


Herramientas del proyecto
Power BI o Tableau
Visualizaciones nativas (barras, líneas, tablas, KPI).
Modelado de datos en esquema estrella.
Cálculos analíticos (medidas y columnas calculadas).

# Etapas del análisis realizadas Paso Acción Resultado para el negocio (Flujo general del proyecto):

Paso	Acción	Resultado
1. Limpieza de datos:	Se validaron tipos de datos, nulos y duplicados para obtener un	dataset listo para análisis.
2. Crear tabla calendario: Se	construyó dim_fecha para análisis temporal el cual es	base para inteligencia de tiempo.
3. Modelado de datos:	Se construyó un esquema estrella como	modelo analítico.
4. Crear medidas:	Se construyeron métricas comerciales e inteligencia de tiempo para los insights del negocio.
5. Diseñar dashboard:	Se crearon páginas de análisis ejecutivo, comercial y cohortes para	visualizaciones claras.
6. Resumen ejecutivo:	Se interpretaron resultados y generaron recomendaciones a modo de insights estratégicos.

Sigue el flujo de trabajo descrito en cada celda del Jupyter Notebook; ahí encontrarás instrucciones paso a paso, pre-código y notas que te servirán de guía para entender el proyecto realizado.

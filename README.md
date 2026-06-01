# RappiPlus: Dashboard Ejecutivo de Rentabilidad y Desempeño Comercial

Proyecto final desarrollado como parte del bootcamp de Data Analytics de TripleTen LATAM.

Este proyecto tiene como objetivo analizar el desempeño comercial de RappiPlus a partir de datos de ventas, costos, marketing, comportamiento de usuarios, retención y experimentación A/B. El análisis permitió transformar datos operativos en insights accionables para evaluar la rentabilidad del negocio, detectar oportunidades de optimización y comunicar los resultados mediante un dashboard interactivo en Tableau.

---

## 📊 Dashboard interactivo

El dashboard final fue desarrollado en Tableau Public y permite explorar los principales indicadores del negocio a través de dos vistas:

* **Overview ejecutivo:** resumen de revenue, profit neto, margen de rentabilidad, costos, inversión en marketing y ticket promedio.
* **Detalle por producto:** exploración de unidades vendidas, revenue, costos y profit operativo, con filtros dinámicos y drill-through por producto.

🔗 https://public.tableau.com/views/Proyecto_Final_Dayana_Rodriguez/Overview?:language=es-ES&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## 🖼️ Vista previa del dashboard

### Overview ejecutivo

![Dashboard Overview](images/dashboard_overview.png)

### Detalle por producto

![Dashboard Detalle](images/dashboard_detalle.png)

---

## 🎯 Objetivo del proyecto

Evaluar el desempeño comercial de RappiPlus mediante un análisis integral de datos que permita responder preguntas clave del negocio:

* ¿El negocio es rentable?
* ¿Cuáles son los principales drivers de revenue, costos y profit?
* ¿En qué etapa del funnel se pierden más usuarios?
* ¿Qué cohortes muestran mayor retención?
* ¿El experimento A/B generó un impacto estadísticamente significativo?
* ¿Cómo comunicar los resultados de forma visual, ejecutiva e interactiva?

---

## 🗂️ Fuentes de datos utilizadas

El proyecto integró múltiples fuentes de datos del negocio:

* `orders_clean.csv`: información depurada de pedidos, usuarios, productos, montos, descuentos, país, dispositivo y fuente de referencia.
* `catalog_clean.csv`: catálogo de productos, categorías, costos unitarios y proveedores.
* `marketing_clean.csv`: inversión en marketing por fecha, país, campaña y canal.
* Datos de eventos, usuarios y actividad para análisis de funnel y retención.
* Datos de experimento A/B para validación estadística.

---

## 🛠️ Herramientas utilizadas

* **Python:** limpieza, transformación, análisis exploratorio y validación estadística.
* **Pandas / NumPy:** manipulación y procesamiento de datos.
* **SciPy / Statsmodels:** pruebas estadísticas para análisis A/B.
* **SQL:** análisis de funnel, comportamiento de usuarios y cohortes.
* **Tableau Public:** construcción del dashboard ejecutivo e interactivo.
* **GitHub:** documentación y publicación del proyecto.

---

## 🔎 Metodología

El proyecto se desarrolló en seis etapas principales:

### 1. Limpieza y validación de datos

Se depuraron los datasets principales, corrigiendo tipos de datos, eliminando duplicados, validando valores inconsistentes y estandarizando variables categóricas.

Principales acciones realizadas:

* Conversión de fechas a formato `datetime`.
* Conversión de variables numéricas.
* Validación de montos, cantidades, descuentos y costos.
* Eliminación de registros inválidos.
* Corrección de inconsistencias en `monto_total`.
* Estandarización de textos en variables categóricas.
* Exportación de datasets limpios para análisis y dashboard.

---

### 2. Análisis de rentabilidad

Se calcularon los principales indicadores financieros del negocio:

* Revenue total.
* Costo total.
* Inversión en marketing.
* Profit neto.
* Margen de rentabilidad.
* Ticket promedio.
* Cantidad promedio de productos por orden.

---

### 3. Análisis de funnel

Se analizó el comportamiento de los usuarios a través de las principales etapas del proceso de conversión:

* First visit.
* Add to cart.
* Select item.
* Begin checkout.
* Add payment info.
* Purchase.

El objetivo fue identificar en qué etapa se produce la mayor pérdida de usuarios y dónde existen oportunidades de optimización.

---

### 4. Análisis de retención por cohortes

Se evaluó la recurrencia de usuarios a partir de cohortes temporales, permitiendo observar patrones de retención y comportamiento posterior a la primera compra.

---

### 5. Análisis A/B

Se aplicaron pruebas estadísticas para evaluar si los cambios propuestos generaron diferencias significativas en el comportamiento de los usuarios.

Se consideraron métricas como:

* Conversión.
* Gasto promedio.
* Diferencias entre grupos de control y prueba.

---

### 6. Dashboard en Tableau

Finalmente, se construyó un dashboard interactivo para comunicar los resultados de forma visual y ejecutiva.

El dashboard incluye:

* KPIs ejecutivos.
* Evolución temporal de revenue y profit.
* Revenue por categoría.
* Profit operativo por categoría.
* Tabla de desempeño por producto.
* Filtros por mes, categoría, país y dispositivo.
* Drill-through desde gráfico de producto hacia tabla de detalle.
* Navegación entre vistas Overview y Detalle.

---

## 📌 Principales KPIs del negocio

| KPI                    | Resultado |
| ---------------------- | --------: |
| Revenue acumulado      |    $9.50M |
| Profit neto            |    $2.84M |
| Margen de rentabilidad |    29.87% |
| Costo total            |    $3.79M |
| Inversión en marketing |    $2.87M |
| Ticket promedio        |      386 |

---

## 💡 Hallazgos principales

### 1. RappiPlus muestra rentabilidad positiva

El negocio presenta un **profit neto de $2.84M** y un **margen de rentabilidad de 29.87%**, lo que evidencia una operación rentable durante el período analizado.

### 2. El revenue se mantiene estable durante 2025

La evolución mensual de revenue y profit muestra un comportamiento relativamente estable, con una caída en febrero y recuperación en los meses posteriores.

### 3. Las categorías presentan una distribución equilibrada

El revenue se distribuye de manera estable entre las categorías principales, sin una dependencia excesiva de una única categoría.

### 4. Existe una alerta comercial en un producto específico

El producto `laptop-gaming-16gb` presenta profit operativo negativo, por lo que se recomienda revisar su estructura de costos, precio unitario o estrategia comercial.

### 5. La principal fricción del funnel ocurre antes del pago

El mayor abandono se detecta entre las etapas `begin_checkout` y `add_payment_info`, lo que sugiere oportunidades de mejora en el formulario o proceso previo al pago.

### 6. El experimento A/B no mostró evidencia suficiente de impacto significativo

Los resultados del experimento no evidenciaron diferencias estadísticamente significativas que justifiquen implementar cambios sin análisis adicional.

---

## ✅ Recomendaciones de negocio

* Revisar la estrategia comercial del producto `laptop-gaming-16gb`, especialmente su costo unitario, precio de venta y margen operativo.
* Optimizar la etapa previa al ingreso de datos de pago, dado que concentra la mayor pérdida de usuarios en el funnel.
* Mantener monitoreo mensual de revenue, profit y margen para detectar desviaciones tempranas.
* Evaluar la eficiencia de la inversión en marketing por canal, priorizando la relación entre gasto, conversión y rentabilidad.
* Complementar futuros experimentos A/B con mayor tamaño muestral o períodos de observación más amplios.

---

## 📁 Estructura del repositorio

```text
rappiplus-dashboard-rentabilidad-tableau/
│
├── README.md
├── Proyecto_Final_RappiPlus.ipynb
│
├── data/
│   ├── orders_clean.csv
│   ├── catalog_clean.csv
│   └── marketing_clean.csv
│
└── images/
    ├── dashboard_overview.png
    └── dashboard_detalle.png
```

---

## 📓 Notebook del análisis

El notebook contiene el desarrollo completo del proyecto, incluyendo limpieza de datos, análisis exploratorio, métricas de rentabilidad, funnel, cohortes, pruebas estadísticas y preparación de los datos para Tableau.

📓 [Ver notebook del proyecto](Proyecto_Final_RappiPlus.ipynb)

> Nota: Debido al tamaño del notebook y la cantidad de salidas generadas durante el análisis, es posible que GitHub no lo renderice correctamente en la vista previa. En ese caso, se recomienda descargar el archivo `.ipynb` o abrirlo desde Google Colab.

---

## 🚀 Conclusión

El análisis evidencia que RappiPlus es un negocio rentable, con revenue estable, margen positivo y oportunidades concretas de optimización en producto, marketing y conversión. El dashboard en Tableau permite monitorear los principales KPIs y profundizar en el desempeño por producto mediante filtros dinámicos y navegación interactiva.

Este proyecto consolida un flujo completo de trabajo analítico: limpieza y validación de datos, análisis exploratorio, evaluación estadística, modelado de indicadores y comunicación ejecutiva mediante visualización interactiva.


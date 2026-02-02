# Análisis de Red de Tiendas RetailNow

Proyecto de análisis de datos para una cadena de tiendas minoristas utilizando Pandas y Numpy. El objetivo es procesar datos de ventas, inventarios y satisfacción del cliente para optimizar el rendimiento de las tiendas.

## Descripción

RetailNow es una cadena de tiendas minoristas que necesita analizar el rendimiento de sus diferentes sucursales. Este proyecto procesa y analiza datos de ventas, inventarios y satisfacción del cliente usando Python con las librerías Pandas y Numpy.

## Estructura del proyecto

```
proyecto/
├── analisis_red_tiendas.ipynb
├── sales.csv
├── inventories.csv
└── satisfaction.csv
```

## Requisitos

- Python 3.x
- Pandas
- Numpy
- Jupyter Notebook

## Archivos de datos

Los datos están distribuidos en tres archivos CSV:

- `sales.csv`: Datos de ventas (ID_Tienda, Producto, Cantidad_Vendida, Precio_Unitario, Fecha_Venta)
- `inventories.csv`: Datos de inventarios (ID_Tienda, Producto, Stock_Disponible, Fecha_Actualización)
- `satisfaction.csv`: Datos de satisfacción del cliente (ID_Tienda, Satisfacción_Promedio, Fecha_Evaluación)

## Análisis realizados

### 1. Carga y limpieza de datos
- Carga de los tres archivos CSV con Pandas
- Eliminación de filas con valores nulos
- Verificación de la estructura de los DataFrames

### 2. Análisis de ventas
- Cálculo de ventas totales por tienda
- Cálculo de ventas totales por producto
- Cálculo de ingresos (Cantidad_Vendida × Precio_Unitario)
- Resumen estadístico de las ventas (media, mediana, desviación estándar)

### 3. Análisis de inventarios
- Cálculo de la rotación de inventarios por tienda
- Identificación de tiendas con inventarios críticos (menos del 10% de ventas respecto al stock)
- Cálculo del porcentaje de productos vendidos

### 4. Análisis de satisfacción del cliente
- Análisis de la satisfacción promedio por tienda
- Identificación de tiendas con satisfacción baja (< 60%)
- Relación entre satisfacción del cliente y ventas
- Recomendaciones para tiendas con baja satisfacción

### 5. Cálculos estadísticos con Numpy
- Conversión de datos de Pandas a arrays de Numpy
- Cálculo de la mediana de las ventas totales
- Cálculo de la desviación estándar de las ventas

### 6. Simulación de proyecciones
- Simulación de ventas futuras para 3 meses usando distribuciones normales
- Uso de seed (42) para reproducibilidad
- Cálculo de estadísticas sobre las proyecciones
- Análisis de crecimiento proyectado

## Resultados principales

El análisis incluye:
- 5 tiendas analizadas
- 3 productos diferentes
- Ventas totales: $50,500
- Mediana de ventas por tienda: $10,500
- 1 tienda con satisfacción baja (Tienda 5 con 55%)
- 0 tiendas con inventarios críticos
- Proyecciones de crecimiento para los próximos 3 meses

## Uso

1. Asegúrate de tener los tres archivos CSV en el mismo directorio que el notebook
2. Abre `analisis_red_tiendas.ipynb` en Jupyter Notebook o Google Colab
3. Ejecuta las celdas secuencialmente

Si usas Google Colab, sube los archivos CSV al entorno antes de ejecutar.

## Notas técnicas

- Las rutas de los archivos están configuradas para uso local. Si usas VSCode con un workspace específico, ajusta las rutas a `/workspace/`
- El código utiliza `np.random.seed(42)` para garantizar resultados reproducibles en las simulaciones
- Los filtros identifican automáticamente tiendas problemáticas según los umbrales establecidos

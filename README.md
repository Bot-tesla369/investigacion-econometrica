# Variables macroeconómicas asociadas a las expectativas económicas a tres meses en el Perú, 2012–2025

Este estudio examina cómo se relacionan el crecimiento del PBI, la inflación subyacente de bienes y la tasa interbancaria con el índice de expectativas de la economía peruana a tres meses.

**Autores** — Belén Belinda Castañeda Casallo, Jhon Kennedy Ibias Mantilla, Emely Dayana Quispe Soto y Daniel Wilder Venancio Romero.  
**Universidad Nacional Federico Villarreal** · Facultad de Ciencias Económicas · Prácticas Preprofesionales II, Grupo 03.

## Datos y modelo

La base reúne 168 observaciones mensuales de BCRPData, de enero de 2012 a diciembre de 2025. El modelo se estima por mínimos cuadrados ordinarios con dos rezagos del índice de expectativas, un indicador para el período de pandemia (marzo de 2020 a diciembre de 2021) y errores estándar Newey–West (HAC) con 12 rezagos. La muestra de estimación contiene 166 observaciones.

| Variable | Medición | Serie BCRP |
| --- | --- | --- |
| Expectativas a tres meses | Índice en puntos, con 50 como nivel neutral | `PD38045AM` |
| Crecimiento del PBI | Variación porcentual interanual | `PN01728AM` |
| Inflación subyacente de bienes | Variación porcentual mensual en Lima Metropolitana | `PN01296PM` |
| Tasa interbancaria | Tasa promedio en moneda nacional, en porcentaje anual | `PN07819NM` |

## Resultados principales

- **Inflación subyacente de bienes.** Un aumento de 0,1 puntos porcentuales en la inflación mensual se asoció con 0,54 puntos menos en el índice de expectativas ese mismo mes (p = 0,008). La asociación de largo plazo también fue negativa (p = 0,012).
- **PBI y tasa interbancaria.** Ninguno mostró una asociación significativa en el mismo mes al 5 %. Para la tasa interbancaria se estimó una asociación negativa de largo plazo, con evidencia limitada (p = 0,046).
- **Contraste conjunto y ajuste.** La prueba de Wald para las tres variables macroeconómicas obtuvo p = 0,026. El R² del modelo fue 0,814. Los resultados se interpretan como asociaciones estadísticas.

## Archivos del repositorio

- [Artículo](paper/) — metodología, resultados y discusión.
- [Base de datos](database/) — archivos de datos, incluida la base final en CSV.
- [Notebook](notebook/) — análisis reproducible en Python.
- [Resultados](resultados/) — 11 tablas y 7 gráficos exportados a PNG.
- [Presentación](presentaci%C3%B3n/) — diapositivas del estudio.
- [Anexos](anexos/) — documentación complementaria.

## Cómo reproducir el análisis

1. Abre `procesamiento.ipynb` en Google Colab o Jupyter.
2. Si usas Jupyter localmente, instala las dependencias con `python -m pip install numpy pandas scipy statsmodels matplotlib`.
3. Ejecuta todas las celdas en orden. El notebook incluye los datos y la carpeta `database/` contiene el CSV de referencia.

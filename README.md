# No registro de ingresos en la EPH – Análisis geoespacial

Este proyecto analiza la distribución geoespacial del **no registro de ingresos** en hogares de la Encuesta Permanente de Hogares (EPH) de Argentina. Se identifican **aglomerados urbanos con alta incidencia de ITF = 0**, y se exploran patrones territoriales asociados al no registro, incluyendo la superposición con zonas de vulnerabilidad estructural (RENABAP).

---

## Objetivo

- Detectar y visualizar territorialmente zonas con alta incidencia de hogares o personas sin ingresos declarados, considerando tanto datos de hogares como de personas, y utilizar herramientas de análisis geoespacial para describir y contextualizar este fenómeno.

---

## Definición conceptual

- **Nivel hogar**: ITF = 0 o no informado.
- **Nivel individual**: personas con P47T = 0 o nulo, pero con condición de actividad declarada (ocupado o desocupado).

---

## Escala de análisis

- Principal: aglomerado urbano (como unidad de análisis espacial).
- Complementaria: provincias, departamentos, municipios y barrios populares RENABAP.

---

## Datasets utilizados

| Nº | Dataset                                 | Fuente                 | Formato | Uso principal                                   |
|----|-----------------------------------------|------------------------|---------|------------------------------------------------|
| 1  | EPH – Hogares                           | INDEC                  | XLSX    | Identificación de hogares sin ingresos         |
| 2  | EPH – Individual                        | INDEC                  | XLSX    | Detección de personas sin ingresos             |
| 3  | Shapefile Provincias                    | IGN                    | SHP     | Referencias regionales                         |
| 4  | Shapefile Departamentos                 | IGN                    | SHP     | Escala intermedia                              |
| 5  | Shapefile Municipios                    | IGN                    | SHP     | Contexto detallado                             |
| 6  | Envolvente urbana aglomerados EPH       | INDEC                  | SHP     | Polígonos para merge espacial                  |
| 7  | Nómina de localidades por aglomerado    | INDEC                  | XLS     | Relación localidades–aglomerado                |
| 8  | Barrios populares RENABAP               | Ministerio Social      | GPKG    | Superposición con zonas de vulnerabilidad      |

---

## Flujo de trabajo (JupyterLab)

1. **Carga y limpieza** de datos EPH.
2. **Identificación de subregistro** (hogares y personas).
3. **Agregación por aglomerado** y cálculo de indicadores.
4. **Unión con shapefiles** y creación de GeoDataFrames.
5. **Visualización geoespacial** (mapas coropléticos).
6. **Análisis espacial y superposición con RENABAP**.

---

## Resultados esperables

- Mapa de aglomerados con mayor incidencia de subregistro.
- Detección de patrones espaciales y zonas críticas.
- Hipótesis interpretativas sobre informalidad o problemas de medición.

---

## Posibles extensiones

- Comparación entre trimestres de la EPH.
- Cruce con indicadores de pobreza multidimensional.
- Análisis discursivo de la informalidad desde medios o políticas públicas.

---

## Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).

---

## Autor

**Alex Colman**  
[independent.academia.edu/AlexColman1](https://independent.academia.edu/AlexColman1)

---

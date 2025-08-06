# FME Datathon 2023 - Sustainable UPC Challenge 🚲🌱

## Análisis de Movilidad Sostenible en la UPC

Este proyecto fue desarrollado para el **FME Datathon 2023**, específicamente para el **Sustainable UPC Challenge**. El objetivo principal es analizar los patrones de movilidad de los estudiantes de la Universitat Politècnica de Catalunya (UPC) y proporcionar insights para promover un transporte más sostenible.

## 📊 Descripción del Proyecto

El proyecto analiza datos de movilidad de estudiantes de la UPC para entender:
- **Patrones de transporte**: Cómo se desplazan los estudiantes entre sus hogares y los diferentes centros de la UPC
- **Preferencias de movilidad**: Qué factores influyen en la elección del medio de transporte
- **Impacto ambiental**: Análisis de la sostenibilidad de los diferentes medios de transporte utilizados
- **Infraestructura existente**: Mapeo de la infraestructura de transporte público y bicicletas

## 🗂️ Estructura del Proyecto

```
├── data/
│   ├── preprocessed.csv              # Datos procesados principales
│   ├── preprocessed_co2.csv          # Datos con métricas de CO2
│   ├── bicis_coordenades.csv         # Coordenadas de estaciones de bicicletas
│   └── coordenades2.csv              # Datos geoespaciales de transporte
├── src/
│   ├── preprocessing.ipynb           # Limpieza y preprocesamiento de datos
│   ├── insights.ipynb                # Análisis estadístico y correlaciones
│   └── plotting.ipynb                # Visualizaciones y mapas interactivos
└── visualisation/
    ├── HTML/                         # Mapas interactivos generados
    │   ├── heatmap.html
    │   ├── circle_lines.html
    │   └── pt_lines.html
    └── PNG/                          # Gráficos estáticos
        ├── heatmap.png
        ├── metro_bike_transportation.png
        └── pt_lines.png
```

## 🔧 Tecnologías Utilizadas

- **Python**: Lenguaje principal de análisis
- **Pandas**: Manipulación y análisis de datos
- **Folium**: Visualizaciones geoespaciales interactivas
- **Matplotlib/Seaborn**: Gráficos estadísticos
- **Shapely**: Procesamiento de datos geométricos
- **Scipy**: Análisis estadístico avanzado

## 📈 Análisis Principales

### 1. Categorización de Transporte
Los medios de transporte se categorizaron en tres grupos:
- **🚗 Transporte Privado**: Vehículos de combustión, eléctricos, motos, taxis
- **🚌 Transporte Público**: Metro, autobús, tren (Renfe), FGC, tranvía
- **🚶 Transporte Activo**: A pie, bicicleta

### 2. Factores de Decisión
Se analizaron los motivos por los cuales los estudiantes eligen cada medio de transporte:
- Rapidez (`r_fastest`)
- Economía (`r_cheapest`) 
- Comodidad (`r_confortable`)
- Única opción disponible (`r_onlyoption`)
- Razones ambientales (`r_environmental`)
- Salud (`r_healthiest`)
- Necesidad de transporte privado (`r_needprivate`)

### 3. Análisis Geoespacial
- **Mapas de calor**: Distribución de estudiantes por código postal
- **Rutas principales**: Conexiones más utilizadas entre residencias y centros UPC
- **Infraestructura**: Ubicación de estaciones de bicicletas y transporte público
- **Análisis temporal**: Estimación de tiempos de viaje según el medio de transporte

## 🗺️ Visualizaciones Principales

### Mapas Interactivos
1. **Mapa de Calor**: Muestra la densidad de estudiantes por área geográfica
2. **Mapa de Flujos**: Visualiza las rutas más populares con flechas proporcionales al número de usuarios
3. **Infraestructura**: Muestra estaciones de bicicletas, paradas de metro y rutas de transporte público

### Análisis Estadísticos
- **Matriz de correlación**: Relaciones entre diferentes factores de decisión
- **Distribución por centros**: Análisis de preferencias de transporte por centro UPC
- **Segmentación demográfica**: Patrones según género, año de estudio, etc.

## 🏃‍♂️ Cómo Ejecutar el Proyecto

### Requisitos
```bash
pip install pandas numpy matplotlib seaborn folium shapely branca scipy
```

### Ejecución
1. **Preprocesamiento**: Ejecutar `src/preprocessing.ipynb`
2. **Análisis**: Ejecutar `src/insights.ipynb`
3. **Visualizaciones**: Ejecutar `src/plotting.ipynb`

## 📊 Principales Hallazgos

### Distribución de Transporte
- **37.2%** de los viajes utilizan transporte activo
- **43.4%** utilizan transporte público
- **19.4%** utilizan transporte privado

### Factores Más Influyentes
1. **Rapidez**: Factor más valorado por los estudiantes
2. **Comodidad**: Segundo factor en importancia
3. **Consideraciones ambientales**: Menor influencia en la decisión

### Patrones Geográficos
- Mayor uso de transporte público en áreas bien conectadas
- Transporte privado predominante en zonas periféricas
- Transporte activo popular en distancias cortas al centro de Barcelona

## 🎯 Impacto y Recomendaciones

### Para la Sostenibilidad
1. **Promoción del transporte activo** en distancias cortas
2. **Mejora de conexiones de transporte público** desde áreas con alta dependencia del transporte privado
3. **Incentivos** para el uso de medios de transporte sostenibles

### Para la Infraestructura
1. **Expansión de la red de bicicletas** en rutas populares
2. **Optimización de horarios** de transporte público según patrones de estudiantes
3. **Puntos de intercambio modal** estratégicamente ubicados

## 👥 Equipo

Proyecto desarrollado como parte del FME Datathon 2023 - Sustainable UPC Challenge.

## 📄 Licencia

Este proyecto fue desarrollado con fines académicos y de investigación para promover la movilidad sostenible en el entorno universitario.

---

*🌍 Contribuyendo a un futuro más sostenible a través del análisis de datos* 🌱

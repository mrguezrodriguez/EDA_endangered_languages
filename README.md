# EDA · Lenguas en Peligro de Extinción

Análisis exploratorio de datos sobre el estado de vitalidad lingüística mundial, cruzando datos de extinción de lenguas con indicadores socioeconómicos por país.

---

## Datasets

| Dataset | Fuente | Filas | Descripción |
|---|---|---|---|
| `extinct-languages.csv` | [Kaggle · The Guardian](https://www.kaggle.com/datasets/the-guardian/extinct-languages) | ~3.500 | Lenguas del mundo con nivel de peligro, número de hablantes y coordenadas geográficas. Fuente original: Atlas UNESCO. |
| `countries-of-the-world.csv` | [Kaggle · fernandol](https://www.kaggle.com/datasets/fernandol/countries-of-the-world) | ~227 | Indicadores económicos y sociales por país: PIB, alfabetización, densidad de población, mortalidad infantil, etc. Fuente: CIA World Factbook. |

Los dos datasets se fusionan por nombre de país en un `df_merged` de ~2.000 filas y ~25 columnas.

---

## Estructura del repositorio

```
EDA_endangered_languages/
│
├── src/
│   ├── data/
│   ├── img/
│   ├── notebooks/
│   └── utils/
│
├── main.ipynb
├── Memoria.pdf
├── Presentacion.pdf
├── .gitignore
└── README.md

---

## Hipótesis analizadas

| # | Tema | Test |
|---|---|---|
| H1 | La distribución del grado de peligro varía según la región del mundo | Chi-cuadrado |
| H2 | Las lenguas con más hablantes tienen menor grado de peligro | Spearman |
| H3 | Los países con mayor PIB tienen lenguas menos amenazadas | Spearman + Kruskal-Wallis |
| H4 | Los países con mayor alfabetización tienen lenguas menos amenazadas | Spearman + Kruskal-Wallis |
| H5 | La variabilidad de hablantes es mayor en Asia que en Europa | Boxplot + IQR |

---

## Tecnologías

- 🐍 Python 3
- 🐼 pandas · numpy
- 📊 matplotlib · seaborn
- 📐 scipy.stats
- 🔬 scikit-posthocs

---

## Cómo ejecutar

1. Clona el repositorio
```bash
git clone https://github.com/mrguezrodriguez/EDA_endangered_languages.git
```

2. Instala las dependencias
```bash
pip install pandas numpy matplotlib seaborn scipy scikit-posthocs
```

3. Abre el notebook
```bash
jupyter notebook src/notebooks/main.ipynb
```

---

## Equipo de trabajo

```
Melania Fondevilla Soler  
María Rodríguez Rodríguez  
William Christopher Walker Robertson  
```

Proyecto desarrollado en el marco del Bootcamp de Data Science 2026.

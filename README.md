# TPE Fundamentos de la Ciencia de Datos 2026

**Trabajo Práctico Especial** — Grupo 07  
Análisis de eficiencia de combustible y emisiones vehiculares con datos de la **EPA (Model Year 2025)**.

**Integrantes:**
- Valentín Delorenzi
- Rocío Migueltorena
- M. del Rosario Coronado

---

## Requisitos previos

- Python **3.10 o superior**
- Git

---

## Instalación paso a paso

### Clonar el repositorio

```bash
git clone https://github.com/mdelrosariocoronado/tpe_fundamentos_2026.git
cd tpe_fundamentos_2026
```

### Crear el entorno virtual

**Linux / Mac:**
```bash
python3 -m venv venv
source venv/bin/activate
```

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

### Instalar las dependencias

```bash
pip install -r requirements.txt
```

### Registrar el entorno como kernel de Jupyter

```bash
python -m ipykernel install --user --name=venv --display-name "Python (venv)"
```

---

## Ejecutar el notebook

```bash
jupyter lab
```

Luego abrí el archivo **`entrega.ipynb`** y verificá que el kernel seleccionado sea **"Python (venv)"** (esquina superior derecha de JupyterLab).

Finalmente: **Restart Kernel & Run All Cells** (`Kernel → Restart Kernel and Run All Cells`).

---

## Estructura del proyecto

```
tpe_fundamentos_2026/
│
├── entrega.ipynb              # Notebook principal de entrega
├── 25-testcar-2026-01-21.xlsx # Dataset original de la EPA (MY 2025)
├── requirements.txt           # Dependencias del proyecto
└── README.md                  # El archivo de configuracion
```

---

## Dependencias principales

| Librería | Uso |
|---|---|
| `pandas` / `numpy` | Manipulación y análisis de datos |
| `scipy` / `statsmodels` | Tests estadísticos (Wilcoxon, Kruskal-Wallis, regresión) |
| `scikit-learn` | PCA, clustering (KMeans), estandarización |
| `matplotlib` / `seaborn` | Visualizaciones |
| `yellowbrick` | Visualización del PCA con biplots |
| `openpyxl` | Lectura del archivo `.xlsx` |

---

## Solución de problemas frecuentes

**Error con `yellowbrick`**
AL instalarse con las dependencias o manualmente en el archivo, requiere _reiniciar_.
**Error `ModuleNotFoundError`:**  
Asegurate de haber activado el entorno virtual y de haber instalado las dependencias con `pip install -r requirements.txt`.

**El kernel no aparece como "Python (venv)":**  
Ejecutá nuevamente el paso 4 (`ipykernel install`) con el entorno virtual activo.

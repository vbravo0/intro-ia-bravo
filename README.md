# Trabajo Final: Introducción a la Inteligencia Artificial

**Autor:** Victor Manuel Bravo Arroyo  
**Diplomatura:** [Diplomatura en Inteligencia Artificial](https://licdia.unlu.edu.ar/dev-ia/) - Universidad Nacional de Luján (UNLu)  
**Curso:** Introducción a la Inteligencia Artificial  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vbravo0/intro-ia-bravo/blob/main/trabajo-final-intro-ia-bravo-victor.ipynb)

---

## ¿De qué se trata el trabajo?

Este trabajo predice el gasto turístico real diario por persona en Argentina usando microdatos de la Encuesta de Viajes y Turismo de los Hogares (EVyTH, relevamiento oficial del Ministerio de Turismo) y el índice de precios al consumidor (IPC del INDEC) del período 2012–2024. Para comparar valores entre años, los montos se deflactan con IPC a precios de 2016 y se transforman a logaritmo. Se limpian los datos, se seleccionan variables por correlación y se comparan dos modelos con partición temporal (entrenamiento 2012–2023 vs. test 2024): Regresión Lineal y Random Forest.

Ambos modelos empatan en desempeño sobre el conjunto de test ($MAE \approx 0.88$, $RMSE \approx 1.14$), por lo que la complejidad del Random Forest no mejora la predicción frente a la regresión lineal ante la caída de ingresos reales de 2024. Los predictores con mayor impacto en el gasto son el tipo de alojamiento (vivienda propia o familiares vs. hotel), el transporte en avión y el tamaño del grupo de viaje.

---

## Estructura del Proyecto

- [`trabajo-final-intro-ia-bravo-victor.ipynb`](trabajo-final-intro-ia-bravo-victor.ipynb): Jupyter Notebook autocontenido con todo el flujo de carga, análisis exploratorio (EDA), preprocesamiento, selección de variables, ajuste de hiperparámetros, entrenamiento temporal y evaluación de interpretabilidad.
- [`requirements.txt`](requirements.txt): Dependencias de Python con sus versiones exactas fijadas.
- **Datos:** Los microdatos oficiales de EVyTH e IPC se descargan automáticamente en la ejecución del notebook desde el paquete empaquetado en [GitHub Releases (v0.1.0)](https://github.com/vbravo0/intro-ia-bravo/releases/tag/v0.1.0) para asegurar reproducibilidad sin bloqueos.

---

## Cómo ejecutar

### Opción 1: Google Colab (Recomendada)
Hacer clic en el botón [Open In Colab](https://colab.research.google.com/github/vbravo0/intro-ia-bravo/blob/main/trabajo-final-intro-ia-bravo-victor.ipynb) y ejecutar las celdas secuencialmente.

### Opción 2: Localmente
```bash
git clone https://github.com/vbravo0/intro-ia-bravo.git
cd intro-ia-bravo
pip install -r requirements.txt
jupyter lab trabajo-final-intro-ia-bravo-victor.ipynb
```

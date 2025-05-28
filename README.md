# 🧥 RopAI — Clasificador y Recomendador de Prendas con IA

Este proyecto aplica técnicas avanzadas de Visión por Computador e Inteligencia Artificial para **clasificar prendas de ropa** e implementar un **sistema de recomendación visual e híbrida**.

### 🎯 ¿Qué hace este proyecto?
- Clasifica imágenes de ropa en más de 13 categorías distintas (camisetas, faldas, pantalones, etc.).
- Recomienda prendas **visualmente similares** usando embeddings de imagen.
- Recomienda prendas según su **color dominante**, eliminando el fondo y analizando el color perceptual.
- Ofrece una recomendación **híbrida**, combinando estilo visual + color.

---

### 🛠️ Tecnologías y herramientas utilizadas

- `TensorFlow / Keras` — para la clasificación con EfficientNetV2-S.
- `FAISS` — para la búsqueda eficiente de imágenes similares.
- `rembg` — para eliminar el fondo de las imágenes.
- `OpenCV` + `KMeans` — para detectar el color dominante.
- `Colormath` — para comparar colores usando la métrica perceptual Delta E (CIE2000).
- `Google Colab` + `Google Drive` — entorno principal de desarrollo y ejecución.
- `pandas` + `gspread` — para exportar resultados a Google Sheets.

---

### ⚠️ Limitaciones importantes

> 🚫 **Este proyecto está diseñado para ejecutarse en mi entorno de Google Drive**, ya que utiliza rutas locales específicas a carpetas con más de 6.000 imágenes clasificadas.

Si deseas utilizarlo por tu cuenta:
- Deberás **entrenar el modelo nuevamente** o ajustar el código para que funcione con tus rutas de imágenes.
- También deberás **reconstruir los índices FAISS** y adaptar el sistema a tu propia estructura de carpetas.

---

### 📁 Notebooks principales

- `FASE1dataaugmentation.ipynb` — Ampliación del dataset y primeros modelos.
- `FASE2.ipynb` — Entrenamiento final y extracción de embeddings visuales.
- `ColorRecomendacion.ipynb` — Recomendación por color con rembg y LAB.
- `Presentacion.ipynb` — Demo final, integración de modelos y exportación a Google Sheets.

---

### 📸 Ejemplo de flujo de uso

1. El usuario sube una imagen de prenda.
2. Se elimina el fondo.
3. Se predice la categoría de la prenda.
4. Se recomienda ropa visualmente similar, por color y por recomendación híbrida.
5. Los resultados se exportan automáticamente a Google Sheets y se pueden visualizar en Locker Studio.

---

¡Gracias por tu interés!  
Este proyecto ha sido desarrollado como trabajo final de máster en IA.



# 🧠 Clasificador de Orientación Política con Gemini

Este módulo automatiza la clasificación de textos transcritos según su orientación política en Argentina (`izquierda`, `derecha`, `neutral`), utilizando inteligencia artificial provista por la API de Google Gemini.

---

## 🎯 Objetivo

El objetivo del sistema es generar etiquetas políticas automatizadas, con justificación argumental, para cada texto analizado. Esta clasificación sirve como punto de comparación frente a modelos propios de aprendizaje automático y análisis discursivo manual.

---

## 📥 Inputs

- Archivos `.txt` en la carpeta `textos/`, cada uno representando un texto periodístico o discurso político.

---

## 📤 Outputs

- Por cada archivo, se genera un `.json` en la carpeta `resultados/` con la siguiente estructura:

```json
{
  "texto_id": "nombre_del_archivo",
  "clasificacion": "izquierda | derecha | neutral",
  "confianza": "alta | media | baja",
  "motivos": ["razón 1", "razón 2", "..."],
  "entidades_mencionadas": ["nombre político", "..."],
  "tokens_procesados": 1234
}
```

- Además, se registra un archivo `log_errores.txt` con errores ocurridos durante el proceso.

---

## 📚 Significado de los campos

- `texto_id`: identificador único del archivo procesado.
- `clasificacion`: etiqueta política determinada por el modelo.
- `confianza`: nivel de certeza expresado por el modelo.
- `motivos`: explicaciones que sustentan la clasificación.
- `entidades_mencionadas`: figuras públicas identificadas en el texto.
- `tokens_procesados`: tokens usados por Gemini para procesar la solicitud.

---

## ⚙️ Tecnologías utilizadas

- Python 3.10+
- Google Gemini API (`google-generativeai`)
- Visual Studio Code
- JSON para salidas estructuradas
- Logging de errores y tokens

---

## ⚡ Ventajas del enfoque

- Clasificación argumentada automática y estandarizada
- Procesamiento en lote de grandes volúmenes de textos
- Integración con otros flujos de trabajo NLP
- Registro de trazabilidad (tokens + logs)
- Ideal para comparar contra modelos supervisados propios

---

## 🧩 Aplicación práctica

Este clasificador es útil para:

- Construcción de datasets anotados automáticamente
- Benchmarking contra clasificadores propios
- Identificación de sesgos discursivos en medios
- Estudios de polarización política en discursos públicos

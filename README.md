```mermaid
mindmap
  root((Opciones Principales LLM "Propio"))
    ::icon(💡)
    1. Entrenar desde Cero
      ::icon(🏗️)
      Descripción: Recolectar datos masivos, diseñar arquit., entrenar (meses, GPUs potentes)
      Pros
        ::icon(✅)
        Control total
        Modelo único potencial
      Contras
        ::icon(❌)
        Costo extremo (millones)
        Requiere datos masivos/calidad
        Requiere equipo experto mundial
      Viabilidad
        ::icon(🎯)
        Grandes tech/instituciones
        Raramente práctico servicios esp.
    2. Afinar (Fine-tuning) Modelo Existente  <-- Asegúrate de que no haya espacios después de esta palabra
      ::icon(⚙️)
      Descripción: Tomar base (Llama, Mistral...), re-entrenar con datos específicos
      Pros
        ::icon(✅)
        Más rápido / económico
        Menos datos / cómputo
        Especialización
        Mantiene capacidades base
      Contras
        ::icon(❌)
        Dependencia base (calidad/licencia)
        Requiere datos específicos/calidad
        Requiere conocimientos ML
        Necesita GPUs (menos)
      Viabilidad
        ::icon(🎯)
        **Opción más común/práctica**
    3. Usar APIs + Prompts + RAG
      ::icon(🔌)
      Descripción: Usar APIs (Gemini, GPT...), personalizar runtime
      Ingeniería de Prompts: Diseño cuidadoso de instrucciones
      RAG (Retrieval-Augmented Generation): Combinar LLM + BBDD propia (Buscar -> Pasar info+pregunta a LLM)
      Pros
        ::icon(✅)
        Más rápido / económico iniciar
        Sin entrenamiento / GPUs dedicadas (pago x uso)
        Incorpora conocimiento actualizado (RAG)
        Menor barrera técnica
      Contras
        ::icon(❌)
        Menos control intrínseco
        Dependencia proveedor externo
        Personalización limitada (prompt/RAG)
        Posible latencia (RAG)
      Viabilidad
        ::icon(🎯)
        Muy viable, a menudo suficiente
        Ideal para incorporar conocimiento esp.
    Pasos Clave para Afinar (Opción 2)
      ::icon(🛠️)
      a. Definir Objetivo/Caso Uso
      b. Elegir Modelo Base (Tamaño, Licencia, Rendimiento, Comunidad)
      c. Preparar Datos (CRÍTICO - Formato, Calidad, Cantidad, Limpieza)
      d. Configurar Entorno (HW: GPUs/Cloud, SW: libs Python)
      e. Realizar Afinamiento (Cargar, Hiperparám., Técnicas eficientes, Ejecutar)
      f. Evaluar Modelo (Métricas auto., **Eval. Humana**)
      g. Desplegar Modelo (API, Infraestructura, Endpoints Cloud)
      h. Monitorizar y Mantener (Rendimiento, Feedback, Re-entrenar)
    Consideraciones Adicionales
      ::icon(⚠️)
      Costo (Cómputo, Almacenamiento, Expertos)
      Experiencia Técnica (ML, Python, Librerías)
      Ética y Seguridad (Contenido dañino/sesgado, Salvaguardas)
      Privacidad de Datos (Cumplimiento GDPR)
```

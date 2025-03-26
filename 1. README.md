# Chatbot-AulaVirtual
Repositorio para el proyecto de chatbot de asistencia en el aula virtual utilizando IA generativa
# Chatbot de Asistencia para el Aula Virtual

## Objetivos
### General:
Desarrollar un chatbot basado en IA generativa para responder dudas frecuentes de estudiantes en el aula virtual.

### Específicos:
1. Implementar Fast Prompting para respuestas precisas.
2. Reducir el tiempo de respuesta en un 50%.
3. Integrar el chatbot en Google Colab y GitHub.

---

## Metodología
1. **Análisis de necesidades**: Recolección de preguntas frecuentes.
2. **Diseño de prompts**: Ejemplo:
   ```python
   prompt = "Responde en menos de 100 tokens: ¿Cuál es la fecha de entrega del TP1?"

##    Implementación: 

Código en Google Colab + Gemini API.
Validación: Pruebas con 3 tipos de consultas (fechas, textos, evaluaciones).

### Herramientas y Tecnologías

| Componente               | Tecnología Utilizada      | Justificación |
|--------------------------|--------------------------|---------------|
| **Modelo de IA**         | Gemini Pro               | Ofrece 60 solicitudes gratuitas por minuto con calidad comparable a GPT-3.5. |
| **Entorno de desarrollo**| Google Colab             | Ejecución en la nube sin configuración local. |
| **Lenguaje de programación** | Python              | Soporte nativo para APIs de IA y amplia documentación. |
| **Control de versiones** | GitHub                  | Plataforma estándar para colaboración y despliegue. |
| **Técnicas de Prompting**| Few-shot learning       | Mejora precisión mediante ejemplos contextuales. |
|                          | Instrucciones claras    | Ej: "Responde como asistente académico en 50 palabras máximo". |
|                          | Limitación de tokens    | Uso de `max_tokens=100` para respuestas concisas. |
| **API**                  | Gemini API              | Gratuita, con fácil integración en Python. |

**Ejemplo de implementación**:
```python
import google.generativeai as genai
genai.configure(api_key="TU_API_KEY")

prompt = """Eres un asistente universitario. Responde en español.
Ejemplo: Pregunta: "¿Cuándo es el parcial?" → Respuesta: "20/11, temas: Cap. 1-3"

Pregunta actual: {}
"""

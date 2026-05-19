# Instrucciones Para Notebooks De NLP

Estas reglas aplican para los proximos notebooks de ejercicios en este proyecto.

## Estilo De Trabajo

- Haz exactamente lo que pide la consigna: nada mas y nada menos.
- Mantén un nivel sencillo/intermedio: claro, interesante, pero sin soluciones demasiado avanzadas (a menos que se pida explicitamentee).
- Respeta el estilo del notebook y los nombres de variables que ya existan.
- No rehagas secciones anteriores si el usuario pide continuar con una parte especifica.
- Si corriges algo anterior, que sea solo porque impide ejecutar lo nuevo.

## Organizacion En Celdas

- No pongas toda una parte en una celda gigante.
- Divide cada seccion en celdas pequeñas y logicas:
  - preparacion o carga
  - funcion o transformacion
  - aplicacion
  - tabla o grafico
  - comentario final si la consigna lo pide
- Usa comentarios breves dentro del codigo para explicar el paso.
- Usa celdas markdown con el mismo estilo del notebook para hallazgos o explicaciones.

## Notebooks

- Edita el `.ipynb` como JSON valido.
- Despues de editar, valida con `python -m json.tool`.
- Si agregas codigo que depende de celdas anteriores, verifica que las variables existan.
- Las celdas deben poder ejecutarse en orden desde arriba.
- No dejes imports despues de usarlos. Ejemplo correcto:

```python
import nltk
nltk.download('recurso', quiet=True)
```

## NLTK

- Antes de descargar un corpus o recurso, intenta verificar si ya existe localmente.
- Si un recurso puede estar como carpeta o `.zip`, revisa ambos para evitar descargas innecesarias.
- Si falta un recurso y la descarga falla por red, pide escalacion para descargarlo.
- Para este proyecto, los recursos pueden incluir:
  - `nps_chat`
  - `opinion_lexicon`
  - `wordnet`
  - `averaged_perceptron_tagger_eng`

## Analisis Y Limpieza

- Conserva siempre el texto original y crea nuevas columnas para versiones limpias.
- No apliques limpiezas agresivas sin necesidad.
- Explica brevemente por que limpiaste algo.
- Para chats, suele ser razonable quitar eventos del sistema como `JOIN`, `PART` y `NICK`.
- Usa pandas de forma simple: `copy`, columnas nuevas, `value_counts`, `head`, `sort_values`, tablas resumen.

## Graficos

- Usa graficos simples y utiles.
- No agregues graficos decorativos si la consigna no los pide.
- Con seaborn, evita advertencias futuras usando `hue` cuando uses `palette`.

## Comentarios

- Los comentarios en markdown deben sonar como estudiante: claros, directos y naturales.
- No exageres la explicacion.
- Evita texto demasiado tecnico si la consigna no lo requiere.
- Si el usuario pide "no tan largo", mantén comentarios y codigo concisos.

## Verificacion

- Ejecuta las celdas nuevas y las dependencias minimas previas cuando sea posible.
- Si no puedes ejecutar algo, dilo claramente.
- No termines dejando sesiones de terminal activas.


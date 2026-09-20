

**Fecha de corte: 8 de septiembre de 2026**

## Contexto

El término Vision-Language-Action adquirió especial relevancia con [RT-2](https://arxiv.org/abs/2307.15818) en 2023. Desde entonces, el campo se ha expandido rápidamente hacia modelos más generales, razonamiento corporizado, monitoreo, seguridad y recuperación de fallos.

Esta revisión no intenta cubrir todo el ecosistema VLA. Selecciona únicamente trabajos cercanos al problema de atribución previa a la acción.

## Línea de tiempo seleccionada

|Fecha|Trabajo|Aporte cercano|
|---|---|---|
|17 ago. 2026|[Security of Foundation-Model-Powered Embodied Agents](https://arxiv.org/abs/2608.16843)|Organiza las superficies de ataque mediante la primera frontera comprometida y reconoce la procedencia del estado como problema abierto.|
|17 ago. 2026|[ESTI](https://arxiv.org/abs/2608.16806)|Demuestra que una representación falsa del entorno puede propagarse desde la entrada del planner hasta la ejecución física.|
|18 ago. 2026|[ManiGuard](https://arxiv.org/abs/2608.17386)|Evalúa restricciones de seguridad durante la ejecución y separa éxito de tarea de comportamiento seguro.|
|27 ago. 2026|[TrapVLA](https://arxiv.org/abs/2608.26578)|Introduce disparadores textuales capaces de producir modos de fallo previamente configurados.|
|31 ago. 2026|[PACT](https://arxiv.org/abs/2609.01662)|Conserva la procedencia conocida de las evidencias antes de autorizar una acción física.|
|1 sep. 2026|[Knowing When to Stop](https://arxiv.org/abs/2609.00908)|Utiliza señales internas para decidir cuándo un action chunk ha perdido suficiente grounding y debe interrumpirse.|
|3 sep. 2026|[FailureSpot](https://arxiv.org/abs/2609.04277)|Detecta fallos VLA antes de ejecutar y localiza temporalmente el inicio de la desviación.|
|4 sep. 2026|[ROBORMBENCH](https://arxiv.org/abs/2609.05401)|Demuestra que el mismo comportamiento puede recibir evaluaciones diferentes al reformular lingüísticamente la meta.|

## Referencias metodológicas complementarias

Otros trabajos recientes aportan elementos útiles para diseñar futuras exploraciones:

- [Evidence-Gated Regularization](https://arxiv.org/abs/2609.03142): estudia la relevancia de diferentes modalidades sensoriales mediante perturbaciones selectivas.
    
- [EmbodiedSkills](https://arxiv.org/abs/2609.01281): registra planificación, ejecución, verificación y recuperación mediante trazas estructuradas.
    
- [What Matters, When?](https://arxiv.org/abs/2609.05376): analiza cómo los distractores visuales afectan distintas fases de una tarea.
    
- [One Word, Different Action](https://arxiv.org/abs/2609.05260): evalúa si una decisión física se mantiene o cambia correctamente ante variaciones lingüísticas.
    
- [LIBERO-RECOVER](https://arxiv.org/abs/2609.05178): estudia recuperación a partir de fallos surgidos durante la ejecución.
    

## Recorte resultante

Estos trabajos ya cubren componentes importantes:

```text
detección
localización temporal
verificación
trazabilidad
procedencia evidencial conocida
interrupción y recuperación
```

Sin embargo, detectar o localizar una desviación no identifica necesariamente su procedencia. Una señal puede originarse en el sistema observado, en las entradas, en la representación del entorno o incluso en el supervisor que produce la evaluación.

Tentacore se concentra en el espacio restante:

```text
desviación de origen desconocido
        ↓
hipótesis de procedencia competidoras
        ↓
evidencia que permita distinguirlas
        ↓
atribución sustentada o abstención
        ↓
decisión antes de la acción física
```

## Posición actual

Hasta la fecha de corte no se ha identificado un trabajo que reúna esta cadena completa en sistemas VLA destinados a entornos domésticos.

Esta conclusión es provisional. El estado del arte continuará actualizándose y, si aparece una investigación equivalente, el recorte de Tentacore deberá revisarse nuevamente.
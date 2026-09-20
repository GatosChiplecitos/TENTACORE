

**Fecha de corte: 8 de septiembre de 2026**

Esta lista reúne los trabajos más cercanos al recorte de Tentacore. La inclusión de un paper no significa que resuelva el mismo problema; indica qué parte del espacio ya está ocupada y qué pregunta permanece abierta.

La mayoría de los trabajos de 2026 son preprints y pueden cambiar en versiones posteriores.

## Referencia base

|Trabajo|Importancia|
|---|---|
|[RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control](https://arxiv.org/abs/2307.15818) — 2023|Referencia histórica para comprender la consolidación de los sistemas Vision-Language-Action.|

## Selección principal

|Fecha|Trabajo|Aporte cercano|Diferencia con Tentacore|
|---|---|---|---|
|17 ago. 2026|[Security of Foundation-Model-Powered Embodied Agents](https://arxiv.org/abs/2608.16843)|Organiza ataques mediante la primera frontera comprometida y reconoce problemas de procedencia del estado.|Presenta una taxonomía; no infiere online el origen de una desviación desconocida.|
|17 ago. 2026|[ESTI — Breaking Planner Integrity Boundary](https://arxiv.org/abs/2608.16806)|Demuestra que información ambiental falsa puede propagarse desde el estado entregado al planner hasta la ejecución.|La corrupción es conocida por el experimento; no se comparan procedencias desconocidas.|
|18 ago. 2026|[ManiGuard](https://arxiv.org/abs/2608.17386)|Verifica restricciones durante la ejecución y separa éxito de tarea de comportamiento seguro.|Identifica qué regla se violó y cuándo, pero no qué componente originó la desviación.|
|27 ago. 2026|[TrapVLA](https://arxiv.org/abs/2608.26578)|Utiliza disparadores textuales para producir modos de fallo físicos configurados.|Conoce el disparador y el fallo inducido; no realiza atribución runtime entre hipótesis.|
|31 ago. 2026|[PACT](https://arxiv.org/abs/2609.01662)|Conserva la procedencia conocida de diferentes evidencias antes de admitir una acción.|Recibe la procedencia como dato; Tentacore investiga la procedencia desconocida del fallo.|
|1 sep. 2026|[Knowing When to Stop](https://arxiv.org/abs/2609.00908)|Detecta mediante señales internas cuándo un action chunk ha perdido grounding suficiente.|La señal permite interrumpir, pero no determina por qué apareció la pérdida de grounding.|
|3 sep. 2026|[FailureSpot](https://arxiv.org/abs/2609.04277)|Detecta fallos antes de ejecutar y localiza temporalmente su inicio.|Localizar el inicio conductual no identifica la procedencia que lo produjo.|
|4 sep. 2026|[ROBORMBENCH](https://arxiv.org/abs/2609.05401)|Demuestra que la misma trayectoria puede recibir evaluaciones diferentes al parafrasear la meta.|Evidencia que el supervisor puede producir una anomalía aparente, pero no adjudica entre todas las procedencias posibles.|

## Referencias complementarias

- [The Verification Gap in Networked Physical AI](https://arxiv.org/abs/2608.19593): separa una propuesta válida de una acción suficientemente respaldada por evidencia.
    
- [EmbodiedSkills](https://arxiv.org/abs/2609.01281): incorpora prerrequisitos, verificación y trazas estructuradas entre planificación y ejecución.
    
- [Evidence-Gated Regularization](https://arxiv.org/abs/2609.03142): utiliza relevancia por sensor y perturbaciones selectivas para estudiar dependencia sensorial.
    
- [What Matters, When?](https://arxiv.org/abs/2609.05376): localiza sensibilidad a distractores visuales según la fase de manipulación.
    
- [One Word, Different Action](https://arxiv.org/abs/2609.05260): evalúa invariancia y sensibilidad ante cambios lingüísticos en decisiones físicas.
    
- [LIBERO-RECOVER](https://arxiv.org/abs/2609.05178): estudia recuperación desde fallos surgidos durante la ejecución.
    
- [RoboSPA](https://arxiv.org/abs/2609.05324): evalúa razonamiento espacial y planificación procedimental con dificultad creciente.
    

## Síntesis

Los trabajos seleccionados cubren detección, localización temporal, verificación, trazabilidad, procedencia evidencial conocida, interrupción y recuperación.

El espacio específico de Tentacore permanece en:

```
desviación de procedencia desconocida
→ hipótesis competidoras
→ evidencia discriminante
→ atribución suficientemente sustentada o indeterminada
→ decisión antes de la acción física
```

Esta selección deberá revisarse periódicamente debido a la velocidad de publicación del campo.
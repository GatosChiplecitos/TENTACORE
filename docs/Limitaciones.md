

Tentacore es una investigación preliminar en desarrollo. Su documentación presenta una pregunta, un recorte y una ruta de trabajo; no un producto terminado ni un sistema de seguridad validado.

## Alcance de los resultados

- Las exploraciones iniciales no permiten demostrar eficacia general.
    
- Una respuesta correcta del modelo no prueba que su razonamiento o atribución sean correctos.
    
- Una señal de anomalía no identifica automáticamente su procedencia.
    
- Las hipótesis obtenidas serán compatibles con la evidencia disponible, no afirmaciones forenses definitivas.
    
- El resultado **indeterminado** deberá conservarse cuando la evidencia no permita distinguir entre explicaciones.
    

## Dependencia de herramientas

La investigación inicial depende de modelos y servicios de terceros, principalmente Gemini Robotics-ER.

Estos servicios pueden cambiar en:

- disponibilidad;
    
- capacidades;
    
- versiones;
    
- límites de uso;
    
- costos;
    
- políticas de acceso;
    
- comportamiento observable.
    

Al tratarse de modelos con acceso limitado a sus procesos internos, parte del análisis deberá realizarse mediante entradas, salidas y eventos disponibles externamente.

## Alcance doméstico

Los resultados estarán limitados a escenas, objetos y tareas del hogar.

No deberán generalizarse automáticamente a:

- fábricas;
    
- hospitales;
    
- vehículos;
    
- almacenes;
    
- espacios públicos;
    
- infraestructura crítica.
    

El Living Lab doméstico mejora la viabilidad del proyecto, pero no representa toda la diversidad de hogares, personas, animales o plataformas robóticas.

## Validación física

Las primeras etapas no incluirán ejecución robótica física. Por ello, no permitirán evaluar completamente movimiento, fuerza, latencia, fallos mecánicos, interacción humana ni consecuencias materiales.

La integración con hardware deberá realizarse posteriormente mediante acciones graduales, reversibles y de bajo riesgo.

## Supervisor y evidencia

Tentacore no considera al supervisor como un observador infalible. La desviación aparente puede originarse en el propio mecanismo de evaluación, en datos desactualizados o en una interpretación incorrecta de la escena.

Más señales concordantes tampoco garantizan mayor evidencia si todas proceden de la misma fuente.

## Ciberseguridad

La aplicación de NIST CSF 2.0 funciona como guía organizativa. No representa cumplimiento formal, auditoría, certificación ni cobertura completa de la seguridad de un robot doméstico.

Tentacore tampoco sustituye controles mecánicos, eléctricos, operacionales o de emergencia.

## Estado del arte

El campo VLA evoluciona rápidamente. Las conclusiones sobre cercanía y novedad dependen de la fecha de corte de la revisión y deberán actualizarse antes de presentar o publicar resultados.

Si aparece un trabajo que cubra el mismo problema, el alcance de Tentacore deberá revisarse nuevamente.

## Divulgación

La publicación abierta estará limitada por privacidad, seguridad y protección de la investigación inédita. No todos los datos, instrucciones, perturbaciones, prompts, umbrales o registros del Living Lab podrán compartirse públicamente.



## Problema de investigación

Los sistemas Vision-Language-Action conectan observaciones visuales e instrucciones en lenguaje con decisiones que pueden convertirse en acciones físicas.

Cuando aparece una desviación observable, detectar que algo no coincide con la tarea esperada no permite determinar automáticamente dónde se originó. Una misma conducta puede ser compatible con problemas en la observación, la representación del entorno, la instrucción, el razonamiento, la planificación, la generación de acciones, el control o incluso el sistema encargado de evaluar al robot.

Por esta razón, una señal de anomalía no debe interpretarse directamente como evidencia de una causa.

Tentacore estudia el momento anterior a la siguiente acción física: qué procedencias continúan siendo compatibles con la evidencia, qué información adicional permitiría distinguirlas y cuándo la atribución debe permanecer indeterminada.

## Pregunta central

> Ante una desviación observable y antes de ejecutar una acción física, ¿Qué hipótesis de procedencia siguen siendo compatibles con la evidencia, qué observaciones permiten distinguirlas y cuándo debe el sistema abstenerse de atribuir un origen?

## Alcance

La investigación se limita a sistemas VLA y capas de razonamiento asociadas dentro de **entornos domésticos**.

El recorte contempla:

- objetos y tareas habituales del hogar;
    
- escenas domésticas controladas;
    
- desviaciones observables antes de la siguiente acción;
    
- comparación de explicaciones alternativas;
    
- búsqueda de evidencia que permita reducir hipótesis;
    
- abstención cuando la evidencia sea insuficiente;
    
- decisiones como continuar, reobservar, solicitar aclaración o detenerse.
    

El entorno doméstico permite mantener un escenario viable y reproducible mediante un Living Lab residencial, sin requerir inicialmente infraestructura robótica especializada.

## Fuera del alcance

Tentacore no pretende:

- detectar todos los fallos posibles;
    
- identificar culpables o actores humanos;
    
- producir atribuciones forenses definitivas;
    
- sustituir controles mecánicos o físicos de seguridad;
    
- certificar que un robot es seguro;
    
- cubrir fábricas, hospitales, vehículos, almacenes o infraestructura crítica;
    
- presentar una señal interna del modelo como prueba automática de causalidad.
    

Los trabajos pertenecientes a otros dominios podrán utilizarse como antecedentes cuando aporten métodos transferibles, pero no ampliarán el ámbito experimental del proyecto.

## Principio de interpretación

```
detectar una desviación ≠ conocer su procedencia
```

Si varias hipótesis continúan explicando lo observado, Tentacore debe conservar la incertidumbre. Declarar **indeterminado** no representa una falla del análisis, sino una decisión responsable ante evidencia insuficiente.
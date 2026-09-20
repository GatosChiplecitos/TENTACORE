

Tentacore utiliza como referencia principal el [NIST Cybersecurity Framework (CSF) 2.0 — traducción oficial al español](https://doi.org/10.6028/NIST.CSWP.29.spa).

NIST CSF 2.0 permite organizar la gestión del riesgo mediante seis funciones:

```
GOVERN → IDENTIFY → PROTECT → DETECT → RESPOND → RECOVER
```

Su aplicación en Tentacore estará adaptada al contexto de robótica doméstica. Esta relación no representa una certificación ni implica que el proyecto cubra por completo todas las categorías del framework.

## Aplicación al entorno doméstico

|Función|Aplicación en Tentacore|
|---|---|
|**Govern**|Definir alcance, responsabilidades, criterios de riesgo, condiciones de colaboración y límites de divulgación.|
|**Identify**|Reconocer datos, sensores, modelos, herramientas, residentes, animales, objetos y dependencias que pueden resultar afectados.|
|**Protect**|Reducir la exposición de credenciales, imágenes, audio, rutinas y datos del hogar; limitar accesos y acciones autorizadas.|
|**Detect**|Observar desviaciones, contradicciones, información desactualizada o señales que no coincidan con la tarea y el estado esperado.|
|**Respond**|Decidir si se continúa, se vuelve a observar, se solicita aclaración, se detiene la acción o se conserva el resultado como indeterminado.|
|**Recover**|Restaurar una condición segura, conservar los registros necesarios, analizar lo ocurrido y actualizar controles o documentación.|

## Posición de Tentacore

El núcleo del proyecto se concentra especialmente en la transición entre **Detect** y **Respond**:

```
desviación observable
        ↓
evaluación de evidencia
        ↓
hipótesis compatibles
        ↓
respuesta antes de la siguiente acción
```

Detectar una desviación no determina automáticamente su origen. Antes de responder, es necesario evaluar si la evidencia permite distinguir entre las procedencias posibles.

## Activos y riesgos considerados

Dentro del entorno doméstico se consideran:

- integridad de observaciones e instrucciones;
    
- vigencia de la información utilizada para decidir;
    
- privacidad de residentes y visitantes;
    
- protección de imágenes, audio y rutinas del hogar;
    
- seguridad de animales y objetos;
    
- acceso a cuentas, modelos, APIs y herramientas;
    
- autorización de acciones físicas;
    
- confiabilidad del sistema supervisor;
    
- dependencia de servicios y modelos de terceros.
    

## Principios de protección

- Minimizar la información doméstica recopilada.
    
- Evitar publicar material identificable.
    
- Separar exploración, simulación y ejecución física.
    
- Conservar supervisión humana y capacidad de detención.
    
- Registrar las versiones y condiciones de las herramientas utilizadas.
    
- No tratar al modelo ni al supervisor como fuentes infalibles.
    
- Abstenerse cuando la evidencia sea insuficiente.
    

## Límite del framework

NIST CSF 2.0 proporciona una estructura para organizar el riesgo, pero no sustituye los estándares técnicos, controles físicos ni evaluaciones específicas que requeriría un sistema robótico completo.

En Tentacore funciona como guía para relacionar la investigación con un proceso reconocible de detección, respuesta y gestión responsable del riesgo.

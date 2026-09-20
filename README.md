# Investigación preliminar sobre la atribución previa a la acción en sistemas VLA en entornos domésticos.

## PROYECTO DE INVESTIGACIÓN APLICADA - TENTACORE

### Descripción general

Tentacore es una investigación aplicada sobre la atribución previa a la acción física en sistemas Vision-Language-Action (VLA) destinados a entornos domésticos.

El proyecto estudia una pregunta concreta: cuando aparece una desviación observable, ¿Qué evidencia permite distinguir dónde pudo originarse antes de que el sistema ejecute la siguiente acción?

El objetivo no es adivinar una causa ni sustituir los controles físicos de seguridad. Tentacore busca conservar las hipótesis compatibles con la evidencia, solicitar más información cuando sea necesario y aceptar indeterminado como resultado válido cuando la procedencia no pueda justificarse.

### Evolución del proyecto

El proyecto comenzó con el nombre "Marco preliminar para evaluar riesgos contextuales preacción en sistemas robóticos con arquitectura VLA".
Durante 2026 el crecimiento del estado del arte fue ocupando diferentes partes de ese planteamiento, aparecieron trabajos sobre detección anticipada a fallos, localización temporal, monitoreo interno, verificación, conservación de procedencia evidencial, replanificación y recuperación.

Este avance no eliminó el problema de investigación, pero se hizo necesario recortarlo con mayor precisión.

Tentacore pasó de una exploración amplia sobre riesgos contextuales a estudiar específicamente la atribución preacción basada en evidencia, cuando varias procedencias todavía pueden explicar la misma desviación.

El alcance también se limitó a entornos domésticos, donde es posible diseñar situaciones reproducibles y desarrollar posteriormente un Living Lab residencial (mi casa) sin depender inicialmente de infraestructura industrial.

### ¿Qué es un sistema VLA?

Los sistemas Vision-language-Action conectan tres elementos: 

observación visual + instrucción de lenguaje + acción física

Estos modelos permiten que un robot interprete una escena, comprenda una instrucción y genere acciones para realizar una tarea.

La investigación que condujo a estos sistemas tiene antecedentes anteriores, pero el término VLA adquirió especial relevancia en 2023 con [RT-2](https://arxiv.org/abs/2307.15818), que conectó conocimiento visual y lingüístico con control robótico.

Desde entonces, el área se ha expandido hacia modelos generales, arquitecturas abiertas, razonamiento corporizado, planificación de tareas, supervisión, seguridad y recuperación de fallos.

### El problema

Una misma desviación física puede ser compatible con diferentes explicaciones:

- Una observación incorrecta o desactualizada
- Degradación o interferencia sensorial
- Una representación equivocada del estado del entorno
- Una instrucción ambigua o manipulada
- Un error de razonamiento o planificación
- Una desviación en la política de acción
- Un problema de ejecución o control
- Una evaluación incorrecta producida por el propio supervisor 

Detectar que una acción parece incorrecta no demuestra cuál de estas posibilidades la originó.

Confundir una señal de anomalía con evidencia causal puede producir una atribución falsa y a partir de ella, una decisión igualmente equivocada.

### Pregunta central

Ante una desviación observable y antes de ejecutar una acción física, ¿qué hipótesis de procedencia siguen siendo compatibles con la evidencia, qué observaciones permiten distinguirlas y cuándo debe el sistema abstenerse de atribuir un origen?

#### Propuesta conceptual 

```text
desviación observable
        ↓
hipótesis compatibles
        ↓
evidencia contrastiva
        ↓
atribución suficientemente sustentada
o resultado indeterminado
        ↓
decisión preacción
``` 

Dependiendo de la evidencia y el riesgo, la decisión podría ser:

- Continuar
- Reobservar
- Solicitar aclaración
- Detenerse
- Declarar procedencia indeterminada 

### Alcance

La investigación está limitada a la robótica doméstica.

Se consideran situaciones relacionadas con objetos, espacios, residentes, animales y actividades habituales del hogar que puedan estudiarse mediante escenarios controlados y reproducibles.

Quedan fuera del alcance:

- Fábricas y almacenes
- Hospitales
- Conducción autónoma 
- Logística
- Infraestructura critica
- Certificación integral de seguridad
- Atribución forense de personas
- Sustitución de controles físicos de emergencia

Los trabajos pertenecientes a otros dominios podrán utilizarse únicamente como antecedentes metodológicos cuando exista una transferencia clara al contexto doméstico. 

### Estado del arte

La literatura reciente ya ha desarrollado mecanismos capaces de:

- Detectar fallos antes de ejecutar
- Localizar temporalmente el inicio de una desviación
- Verificar restricciones de seguridad
- Conservar trazas entre planificación y ejecución
- Estimar relevancia sensorial
- Decidir cuándo detener o truncar una acción
- Recuperar tareas después de un fallo
- Conservar procedencia evidencial previamente conocida

Entre los trabajos cercanos se encuentran:

- [Security of Foundation-Model-Powered Embodied Agents](https://arxiv.org/abs/2608.16843)
    
- [ESTI](https://arxiv.org/abs/2608.16806)
    
- [ManiGuard](https://arxiv.org/abs/2608.17386)
    
- [TrapVLA](https://arxiv.org/abs/2608.26578)
    
- [PACT](https://arxiv.org/abs/2609.01662)
    
- [Knowing When to Stop](https://arxiv.org/abs/2609.00908)
    
- [FailureSpot](https://arxiv.org/abs/2609.04277)
    
- [ROBORMBENCH](https://arxiv.org/abs/2609.05401) 

Hasta la fecha de corte de esta revisión, no se ha identificado un trabajo que reúna la cadena completa estudiada por Tentacore:

```text
procedencia desconocida
→ hipótesis competidoras
→ evidencia discriminante
→ atribución o abstención
→ decisión antes de la acción física
```

Esta conclusión es provisional y deberá actualizarse conforme evolucione el campo.

### Herramientas y factibilidad inicial

Las primeras exploraciones se realizaron con [Gemini Robotics-ER 1.6](https://deepmind.google/blog/gemini-robotics-er-1-6/) mediante Google AI Studio.

El proyecto continuará con Gemini Robotics-ER 2, la generación vigente del modelo de razonamiento corporizado de Google: ER 2 funciona como una capa de razonamiento y orquestación, no debe de confundirse con un VLA de control motor.

Recursos oficiales:

- [Gemini Robotics-ER 1.6](https://deepmind.google/blog/gemini-robotics-er-1-6/)
    
- [Model card de ER 1.6](https://deepmind.google/models/model-cards/gemini-robotics-er-1-6/)
    
- [Presentación de Gemini Robotics-ER 2 en español](https://blog.google/intl/es-419/noticias-de-la-empresa/tecnologia/gemini-robotics-er-2/)
    
- [Documentación de Gemini Robotics-ER](https://ai.google.dev/gemini-api/docs/robotics-overview?hl=es-419)
    
- [Ficha técnica de ER 2](https://ai.google.dev/gemini-api/docs/models/gemini-robotics-er-2-preview)

La etapa inicial puede desarrollarse con una computadora, conexión a internet, acceso al modelo y escenas domésticas controladas. No requiere adquirir inicialmente un robot, construir un laboratorio especializado ni utilizar software de alto costo. El acceso a los modelos puede estar sujeto a disponibilidad, cuotas y consumo de créditos.

### Framework de ciberseguridad

Tentacore utiliza como referencia principal el NIST Cybersecurity Framework (CSF) 2.0:

- [Traducción oficial al español](https://doi.org/10.6028/NIST.CSWP.29.spa)
- [Publicación oficial](https://csrc.nist.gov/pubs/cswp/29/the-nist-cybersecurity-framework-csf-20/final)

Adaptado al contexto de la robótica doméstica, este framework se relaciona especialmente con la transición:


```text
DETECT
   ↓
evaluar evidencia y riesgo
   ↓
RESPOND antes de la siguiente acción
```

El framework permite organizar activos, riesgos, controles, responsabilidades, detección, respuesta y recuperación sin presentar Tentacore como sustituto integral del sistema robótico.

### Resultado y estado actual 

Tentacore se encuentra en fase de investigación, actualmente cuenta con 

- Problema y alcance definidos
- Pregunta central delimitada
- Revisión del estado del arte
- Herramienta inicial identificada
- Framework de ciberseguridad seleccionado
- Hoja de ruta para exploraciones posteriores

Este repositorio no presenta todavía un producto terminado, una implementación validad ni resultados experimentales concluyentes.

### Contenido del repositorio

La documentación se organiza en:

- Problema y alcance
- Estado del arte
- Herramientas y factibilidad
- Hoja de ruta
- Framework de ciberseguridad
- Limitaciones
- Papers seleccionados

### Divulgación responsable

El repositorio puede publicar el problema, el alcance, la pregunta de investigación, el estado del arte, la arquitectura conceptual y los avances autorizados.

Durante la fase de investigación permanecerán reservados los instrumentos inéditos, reglas exactas, firmas internas, perturbaciones operacionales, prompts, umbrales, datos crudos del hogar y resultados que puedan comprometer la privacidad o el trabajo futuro. 

### Autoría

##### Ana Karen Ramos González
Investigación independiente

Tentacore es un proyecto de investigación aplicada en curso. La mención de modelos, empresa o frameworks externos no implica afiliación, respaldo ni certificación por parte de sus desarrolladores.
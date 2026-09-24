# Tarea: Mi prompt profesional

## Funcionalidad elegida

Calculo de notas

## Version 1: prompt basico

El prompt base, muy genérico y abierto.

Al no especificar ningún dominio ni requerimiento, la IA no tiene contexto sobre qué tipo de programa crear.

Apenas ofrece valor específico. La IA suele generar un "Hola Mundo" básico o un ejemplo trivial (como una calculadora simple o una clase genérica aleatoria), ya que tiene que adivinar por completo la intención del usuario.

```text
Actua como desarrollador Java. Crea un programa en Java.

```

## Version 2

Qué cambió: Se añadió el objetivo específico del programa ("gestionar el cálculo de notas de un estudiante").

Por qué: Se le da un caso de uso real a la IA, limitando el campo de acción al dominio educativo/académico.

Qué mejoró en la respuesta: La IA ya genera un programa funcional orientado al problema. Creará una estructura lógica relacionada con notas , pero la arquitectura interna (atributos, diseño de clases) queda a libre criterio de la IA.

```text
Actua como desarrollador Java. Crea un programa en Java para gestionar el calulo de notas de un estudiante
```

## Version 3: prompt final

Qué cambió: Se especificó el diseño técnico detallado (atributos obligatorios), el orden de entrega de la información (explicación primero, código después) y restricciones de estilo/visibilidad para el código (nombres de métodos get/set específicos y modificadores de acceso como private int[] notas).

Por qué: Se redujo al mínimo la ambigüedad, aplicando buenas prácticas de ingeniería de prompts (rol + contexto + requerimientos técnicos + formato de salida).

Qué mejoró en la respuesta: La respuesta es altamente precisa, predecible y útil, el código con la arquitectura de clases que se requiere, explicada paso a paso y respetando las convenciones de encapsulamiento y nomenclatura que se solicito, evitando tener que pedir correcciones posteriores.

```text
Actua como desarrollador Java. Crea un programa en Java para gestionar el calulo de notas de un estudiante usando una clase Estudiante con los atributos codigo, nombre, edad, grado ,notas . Explica primero la estructura de la clase y luego presenta el codigo Java y Usa este estilo para los metodos: getNombre(), setGrado(int grado), private int[] notas.

```

## Componentes del prompt final

| Componente  | Texto de mi prompt                                                                                                                                                  |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Rol         | Actua como desarrollador Java                                                                                                                                       |
| Instruccion | Crea un programa en Java                                                                                                                                            |
| Contexto    | para gestionar el cálculo de notas de un estudiante                                                                                                                 |
| Ejemplo     | usando una clase Estudiante con los atributos codigo, nombre, edad, grado, notas                                                                                    |
| Formato     | Explica primero la estructura de la clase y luego presenta el codigo Java. Usa este estilo para los metodos: getNombre(), setGrado(int grado), private int[] notas. |

## Evaluacion del resultado

| Criterio                            | Prompt |
| ----------------------------------- | ------ |
| Menciona el objetivo del sistema    | si     |
| Menciona a los usuarios principales | si     |
| Tiene exactamente 3 funcionalidades | no     |
| Esta en 3 parrafos                  | si     |
| Lo usaria en un informe real        | no     |

## Errores que evite

1. Ser demasiado general / Cómo se evitó: El prompt inicial era demasiado abierto ("Crea un programa en Java"). En el prompt final se corrigió especificando exactamente qué tipo de programa se requería, limitándolo al dominio de gestionar el cálculo de notas de un estudiante y detallando la clase Estudiante con sus atributos específicos (codigo, nombre, edad, grado, notas). Esto eliminó la ambigüedad y obligó a la IA a generar un caso de uso concreto y útil.

2. No indicar el formato / Cómo se evitó: En lugar de dejar que la IA organizara la respuesta de forma aleatoria, el prompt final incluyó una instrucción de estructura explícita: "Explica primero la estructura de la clase y luego presenta el codigo Java". Además, se especificó un estilo de nomenclatura y visibilidad obligatorio para los métodos y atributos (getNombre(), setGrado(int grado), private int[] notas). Esto garantizó que la presentación y el formato del código coincidieran exactamente con lo esperado.

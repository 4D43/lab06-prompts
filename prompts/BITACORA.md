# Bitacora de prompts
 
Laboratorio 06: Fundamentos de Ingenieria de Prompts.
 
Herramienta de IA usada: (escribe aqui cual usaste)

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. |35|7 |
| The students program in Java. |31 |6 |
| desafortunadamente |19 |5 |

Al llenar la ventana de contexto, con el nombre y la tecnologia que usa la aplicacion la IA toma la informacion basica sobre el proyecto, pero solo este chat tiene el contexto (no comparte la memoria) si se hace alguna apregunta sobre el proyecto en otro el chat no sabra que responder.   
 
## Ejercicio 3: Temperatura
 
| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 |100.0 |BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 |65.3 |BiblioTec, BiblioTec, BiblioTec, BiblioTec, LibroYa |
| 1 |44.5 |LibroYa, BiblioTec, LibroYa, PrestaLibro, PrestaLibro |
| 1.8 |32.2 |PrestaLibro, NubeDeTinta, LibroYa, PaginaLibre, BiblioTec |

Al aumentar la temperatura, la variedad de los nombres se incrementa, con temperatura 0 siempre se elige la opcion con mayor probalbilidad. Con temperaturas mayores se suaviza la distribucion de probabilidad de palabras y se le da opurtunidad a opciones menos problables pero creativas.         

## Ejercicio 4: Prompt vago vs estructurado

| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema |si |si |
| Menciona a los usuarios principales |no |si |
| Tiene exactamente 3 funcionalidades |no |si |
| Esta en 3 parrafos |no |si |
| Lo usaria en un informe real |no |si |

 
## Ejercicio 5: Anatomia de un prompt

| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol |Actua como desarrollador Java |
| Instruccion |Crea un programa en Java |
| Contexto |para gestionar los productos de una tienda |
| Ejemplo |usando una clase Producto con los atributos codigo, nombre, precio y stock |
| Formato |Explica primero la estructura de la clase y luego presenta el codigo Java. Usa este estilo para los metodos: getPrecio(), setPrecio(double precio). |

## Ejercicio 6: Del prompt basico al profesional

```text
Actua como desarrollador Java. Crea un ejemplo de login para una
aplicacion de escritorio utilizando Swing. El usuario debe ingresar
correo y contrasena. Explica brevemente el funcionamiento y presenta
el codigo organizado por clases.

Mejora el codigo anterior con estas restricciones: no uses librerias
externas, valida que el correo contenga @ y que la contrasena tenga
al menos 8 caracteres, y muestra los mensajes con JOptionPane.

```



# Mundos Virtuales. Introducción a la programación de gráficos 3D.
 ## Tarea del seminario de Mundos Virtuales de la asignatura de Interfaces Inteligentes de la ULL

 ## Autor: David Arteaga Sánchez

 ### 1. Qué funciones se pueden usar en los scripts de Unity para llevar a cabo traslaciones, rotaciones y escalados.

 - Traslaciones: `Transform.Translate()`
 - Rotaciones: `Transform.Rotate()`
 - Escalados: `Transform.localScale`
  
 ### 2. ¿Cómo duplicarías el tamaño de un objeto en en un script?.

 `transform = GetComponent<Transform>();
 transform.localScale -= 2;`

 ### 3. Cómo situarías un objeto en la posición (3,5,1)

 `transform = GetComponent<Transform>()
 transform.position = new Vector3(3,5,1)`
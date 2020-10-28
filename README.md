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

 `transform = GetComponent<Transform>();  

 transform.position = new Vector3(3,5,1);`

 ### 4. Como trasladarías 3 metros en cada uno de los ejes y luego lo rotas 30º alrededor del eje Y?

 `transform = GetComponent<Transform>();

 transform.Translate(3,3,3);

 transform.Rotate(0.0f, 30.0f, 0.0f);`

 ### 5. Como rotarías un objeto sobre el eje (1,1,1)

 `transform = GetComponent<Transform>();

 transform.Rotate(30.0f, 30.0f, 30.0f);`

 ### 6. Rota un objeto alrededor del eje Y 30ª y desplázalo 3 metros en cada uno de los ejes. ¿Obtendrías el 
 mismo resultado que en 4?

 No, ya que al realizar primero la rotación, el sistema de referencia local del objeto cambia, por lo que al
 realizar la traslación lo estaremos haciendo hacia direcciones distintas. 

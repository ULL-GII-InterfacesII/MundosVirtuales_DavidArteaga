# Mundos Virtuales. Introducci�n a la programaci�n de gr�ficos 3D.
 ## Tarea del seminario de Mundos Virtuales de la asignatura de Interfaces Inteligentes de la ULL

 ## Autor: David Arteaga S�nchez

 ### 1. Qu� funciones se pueden usar en los scripts de Unity para llevar a cabo traslaciones, rotaciones y escalados.

 - Traslaciones: `Transform.Translate()`
 - Rotaciones: `Transform.Rotate()`
 - Escalados: `Transform.localScale`
  
 ### 2. �C�mo duplicar�as el tama�o de un objeto en en un script?.

 `transform = GetComponent<Transform>();  

 transform.localScale -= 2;`

 ### 3. C�mo situar�as un objeto en la posici�n (3,5,1)

 `transform = GetComponent<Transform>(); ` 

 `transform.position = new Vector3(3,5,1);`

 ### 4. Como trasladar�as 3 metros en cada uno de los ejes y luego lo rotas 30� alrededor del eje Y?

 `transform = GetComponent<Transform>();`

 `transform.Translate(3,3,3);`

 `transform.Rotate(0.0f, 30.0f, 0.0f);`

 ### 5. Como rotar�as un objeto sobre el eje (1,1,1)

 `transform = GetComponent<Transform>();`

 `transform.Rotate(30.0f, 30.0f, 30.0f);`

 ### 6. Rota un objeto alrededor del eje Y 30� y despl�zalo 3 metros en cada uno de los ejes. �Obtendr�as el 
 mismo resultado que en 4?

 No, ya que al realizar primero la rotaci�n, el sistema de referencia local del objeto cambia, por lo que al
 realizar la traslaci�n lo estaremos haciendo hacia direcciones distintas. 

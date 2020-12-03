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

 `transform.Rotate(0.0, 30.0, 0.0);`

 ### 5. Como rotar�as un objeto sobre el eje (1,1,1)

 `transform = GetComponent<Transform>();`

 `transform.Rotate(30.0, 30.0, 30.0);`

 ### 6. Rota un objeto alrededor del eje Y 30� y despl�zalo 3 metros en cada uno de los ejes. �Obtendr�as el mismo resultado que en 4?

 No, ya que al realizar primero la rotaci�n, el sistema de referencia local del objeto cambia, por lo que al
 realizar la traslaci�n lo estaremos haciendo hacia direcciones distintas. 

 ### 7. Como puedes obtener la distancia al plano cerca del volumen de vista desde la c�mara

 `camera = GetComponent<Camera>()`
 `camera.nearClipPlane;`

 ### 8. Como puedes aumentar el �ngulo de la c�mara

 `camera = GetComponent<Camera>();`
 `camera.fieldOfView += x;`

 ### 9. Qu� efecto tiene disminuir el �ngulo de la c�mara.

 Se disminuye el campo de visi�n por lo que se ver�n menos objetos de la escena, sin embargo, estos parecer�n mucho m�s grandes.

 ### 10. Configura un volumen de vista que recorte objetos de la escena.

 Para lograrlo modificamos el �ngulo de la camara hasta encajar el objeto en la posici�n que queramos.

 ### 11. Como puedes realizar la proyecci�n al espacio 2D

 Cambiando el valor de proyecci�n a Ortographic en las propiedades de la clase Camera.

 ### 12. Especifica la rotaci�n de los apartados 4 y 6 con la utilidad quaternion.

 `transform = GetComponent<Transform>()`
 `transform.rotation = Quaternion.Euler(0, 30, 0)`

 ### 13. �Como puedes averiguar la matriz de proyecci�n en perspectiva que se ha usado para proyectar la escena al �ltimo frame renderizado?
 
 Con la propiedad `previousViewProjectionMatrix` de Camera.

 ### 14. �Como puedes averiguar la matriz de proyecci�n en perspectiva ortogr�fica que se ha usado para proyectar la escena al �ltimo frame renderizado?

 Con la propiedad anterior pero con la vista ortogonal activada.

 ### 15. �C�mo puedes obtener la matriz de transformaci�n entre el sistema de coordenadas local y el mundial?.

 - Local: `cameraToWorldMatrix` del component Camera.
 - Mundial: `localToWorldMatrix` del component Transform.

 ### 16. C�mo puedes obtener la matriz para cambiar al sistema de referencia de vista

 Usando la propiedad localToWorldMatrix del component Transform.

 ### 17. Especifica la matriz de la proyecci�n usado en un instante de la ejecuci�n del ejercicio 1 de la pr�ctica 1.


 ### 18. Especifica la matriz de modelo y vista de la escena del ejercicio 1 de la pr�ctica 1.


 ### 19. Aplica una rotaci�n en el start de uno de los objetos de la escena y muestra la matriz de cambio al sistema de referencias mundial.


 ### 20. �Como puedes calcular las coordenadas del sistema de referencia de un objeto con las siguientes propiedades del Transform:?: Position (3, 1, 1), Rotation (45, 0, 45)


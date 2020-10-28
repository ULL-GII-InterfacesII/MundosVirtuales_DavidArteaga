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

		`transform = GetComponent<Transform>()
		transform.position = new Vector3(3,5,1)`
# Práctica 2 - Introducción a los scripts y física en Unity
## Gerard Antony Caramazza Vilá
### 1. Crear una escena simple sobre la que probar diferentes configuraciones de objetos físicos en Unity. La escena debe tener un plano a modo de suelo, una esfera y un cubo.
- a) Ninguno de los objetos será físico.

  Ambos objetos se quedan suspendidos en el espacio sin caer:
![Ninguno de los objetos será físico](https://i.gyazo.com/fefd1f634c8f310f8b780b45d0607280.gif)

- b) La esfera tiene físicas, el cubo no.

  La esfera al tener físicas cae colisionando con el plano, mientras que el cubo se queda suspendido:
  ![La esfera tiene físicas, el cubo no](https://i.gyazo.com/fc41656454fa0a7f63e72a78461fad16.gif)

- c) La esfera y el cubo tienen físicas.

  Al tener ambos objetos físicas, éstos caen y colisionan con el plano:
  ![La esfera y el cubo tienen físicas](https://i.gyazo.com/94f53fd0f31dbc9c6f76889cb3548228.gif)

- d) La esfera y el cubo son físicos y la esfera tiene 10 veces la masa del cubo.

  La esfera al tener mayor masa deforma levemente el cuadrado al colisionar con éste lo que preduce un efecto de rebote que hace que la esfera entre en movimiento:
  ![La esfera y el cubo son físicos y la esfera tiene 10 veces la masa del cubo](https://i.gyazo.com/4d6974e81e86f8b93bd83dbb15735178.gif)

- e) La esfera tiene físicas y el cubo es de tipo IsTrigger.

  Con el fin de apreciar mejor esta configuración se ha desarrollado el siguiente script en C#:
  ```c#
  // Show message when object collider has been triggered
  void OnTriggerEnter() 
  {
    Debug.Log("Object collider has been triggered!");
  }
  ```
  El cubo se encuentra suspendido y cuando la esfera colisiona con éste se muestra un mensaje en la consola con el texto **"Object collider has been triggered!"**:
  ![La esfera tiene físicas y el cubo es de tipo IsTrigger](https://i.gyazo.com/912ca063bae50c4f1ade722db4b99696.gif)

- f) La esfera tiene físicas, el cubo es de tipo IsTrigger y tiene físicas.

  El cubo se encuentra suspendido y cuando la esfera colisiona con éste se muestra un mensaje en la consola con el texto **"Object collider has been triggered!"**:
  ![La esfera tiene físicas y el cubo es de tipo IsTrigger](https://i.gyazo.com/912ca063bae50c4f1ade722db4b99696.gif)
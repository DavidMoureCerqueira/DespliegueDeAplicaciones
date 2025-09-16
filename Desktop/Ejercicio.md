probad los siguientes casos. Crea ficheros nuevos o haz cambios en los existentes:

- ¿Qué pasa si hacemos un add, un commit y después nos equivocamos y hacemos pull en vez de push?
  Compruébalo haciendo modificaciones en los archivos desde GITHUB.

En caso de equivocacion, no pasa nada, porque git comprueba que esta al dia el head con el github

- ¿qué ocurre si hacemos add y después modificamos el archivo y hacemos commit sin volver a hacer add?.
  Compruébalo.

Te avisa de que no hay cambios, o que no se han añadido

- ¿qué ocurre si hacemos add, y después hacemos pull y checkout?. Compruébalo. Aquí intervienen las ramas,
  ya las iremos viendo…
  Te dice que tu rama (head) está por delante del main en un commit

- ¿Cuándo hacemos push se eliminan los commits si ha sido exitoso? Compruébalo con el comando git log

No, se almacenan

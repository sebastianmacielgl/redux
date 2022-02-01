## Redux

Redux es un contenedor de estado predecible para Javascript, como su web lo declara. Si bien está más asociado con React generalmente, puede utilizarse con Javascript sin ningún framework o librería extra.

La idea básica de redux es agregar más opciones al manejo de estado en una aplicación. También la idea es agregar facilidades, mejor acceso y control.
Por otro lado nos presenta la idea de compartir el estado hacia todos los lugares de nuestra aplicación. Evitar el prop drilling en React, y tener más ordenado el estado como consecuencia.

Se basa en la idea de inmutabilidad de datos. Al modificar el estado, lo que realmente sucede es que se hace una copia del estado, esa copia es la que recibe las modificaciones correspondientes, y siempre terminamos entregando a la aplicación esa copia modificada y actualizada. Esto resuelve el problema de inconsistencias en los datos gracias a la inmutabilidad.

## Context (ReactJS)

La API de Context nos proveen básicamente la misma idea de compartir y centralizar el estado en toda la aplicación.
Para usar Context, React nos brinda el Hook que sirve para consultar el estado actual de nuestro contexto, porque podemos tener varios contextos aislados de hecho.
La realidad es que generalmente se utiliza para compartir estado en nuestra app. Si bien puede modificarse el estado, React no provee por defecto una manera de realizarlo, pero podemos crear funciones y maneras de actualizar el context.

## Cosas en común

Tanto Context como Redux manejan el estado de tres maneras. Creando el estado, proveyendo el estado y consumiendo/modificando el estado.
En este sentido nos referimos a que en los dos, tenemos que envolver con un proveedor todos los componentes en los cuales queramos tener acceso al estado.
Generalmente, se utiliza estos wrappers en el nivel más alto de la jerarquía de componentes, para así poder disponer de los datos desde dónde sea en la app.

## Diferencias

Una de las dos diferencias más grandes es que Redux viene de fábrica con maneras de cambiar el estado. Y por otro lado, la complejidad de implementar cada uno varía fuertemente. Una queja común de Redux es que el boilerplate y la curva de aprendizaje suele ser bastante intenso. Context es más simple y por lo tanto más fácil de implementar, teniendo en cuenta las falencias de flexibilidad que goza Redux

## Cuándo usar Context o Redux

Se recomienda que el uso de context sea contemplado en una aplicación poco compleja, si bien Context puede utilizarse realmente en grandes aplicaciones, a la hora de la modificación de datos u otros detalles, puede llevar a tener que crear soluciones personalizadas para cada caso de uso.

Redux por otro lado, cuenta hasta con un toolkit para el manejo integral del estado, esto es, ya nos provee por default de manera de cambiar el estado, y asegurándonos la estabilidad. Otra ventaja, es que es muy común el uso de otras librerías paralelas, como Redux Thunk, que le da a redux la habilidad de por ejemplo hacer llamadas asincrónicas directamente desde el ecosistema de Redux. Y por otro lado, una librería para persistir el estado, generalmente en LocalStorage, lo cual se recomienda encriptar la información si es sensible, que también existe una librería para cumplir ese propósito.

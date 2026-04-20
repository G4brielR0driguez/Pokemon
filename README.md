# Pokemon

1. ¿Por qué el estado vive en App?

El estado de la lista vive en App porque es el componente raíz y el que obtiene los datos desde la API. Desde ahí se distribuye hacia los demás componentes mediante props. Esto evita duplicar lógica y mantiene una única fuente de verdad.

2. Diferencia entre presentacional y contenedor

Un componente contenedor maneja lógica y estado, mientras que uno presentacional solo muestra datos.

App: contenedor
PokemonList: presentacional
PokemonCard: contenedor
3. Problema sin [name]

Si no se agrega [name] como dependencia, el fetch solo se ejecuta una vez y no se actualizaría cuando cambie el Pokémon, mostrando datos incorrectos.

4. Dos interfaces distintas

Se usan dos porque cada endpoint devuelve estructuras diferentes. Separarlas evita errores y hace más claro el tipado.

5. Ventaja de PokemonList sin API

Permite reutilizar el componente con cualquier lista de datos sin depender de cómo se obtienen. También facilita el testing porque no necesita mocks de fetch.

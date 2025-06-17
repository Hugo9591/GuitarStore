# Tienda de Guitarras

Web donde se pueden explorar varios modelos de guitarra, añadirlos a un carrito y comprar, toda la informacio de las guitarras esta en un archivo aparte almacenado en un 
array de objetos, al agregar una guitarra al carrito se guarda en localStorage, de modo que no desaparece la informacion al cerrar el navegador.

## Funciones destacadas
- Guitarras: lista dinámica con foto, nombre, descripción y precio de cada guitarra.  
- Carrito persistente 
  - Agregar / quitar unidades desde el propio carrito.  
  - Actualiza el total gracias a un `useState` (sin recargar la página).  
  - Quitar un solo artículo con el icono 'x' o vaciar todo el carrito con un solo clic con un boton en la parte inferior del carrito.  

## Tecnologías
React: Interfaz y lógica
Vite: Empaquetado ultrarrápido
TypeScript: Tipado estático
CSS (Tailwind):E stilos

## Instalación rápida

git clone https://github.com/Hugo9591/GuitarStore.git
cd tu-repo
npm install       # o pnpm install / yarn
npm run dev
Luego abre http://localhost:5173


## Cómo funciona
Al pulsar “Añadir al carrito”, se guarda { foto, nombre, precio y cantidad }.

Ese estado se sincroniza con localStorage usando un useEffect.

Cada cambio recalcula el total, si se agregan mas guitarras o si  se modifica la cantidad del prodcuto.

Si el usuario pulsa 'x' se elimina el elemento del carrito.

“Vaciar carrito” sencillamente limpia el array y el storage.

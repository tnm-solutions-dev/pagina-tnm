# 📋 Guía: Cómo agregar clientes

## Ubicación del código
El array de clientes está en **index.html** (línea ~515)

## Estructura de un cliente
```javascript
{
    nombre: "Nombre del Cliente",
    sistemas: [
        { nombre: "MenuMaster", url: "https://tu-sitio.com/menu" },
        { nombre: "Gestium" } // sin url si es privado
    ],
    logo: "C1",  // O: "imagenes/logo-cliente.png"
    descripcion: "Descripción o rubro del negocio"
}
```

También puedes seguir usando el formato anterior si solo quieres mostrar texto:
```javascript
{
    nombre: "Nombre del Cliente",
    sistema: "MenuMaster, Gestium",
    logo: "C1",
    descripcion: "Descripción o rubro del negocio"
}
```

## Cómo agregar un cliente (Ejemplo)

### Opción 1: Con iniciales (más rápido)
```javascript
{
    nombre: "El Comidón",
    sistema: "MenuMaster",
    logo: "EC",  // Mostará "EC" en un cuadrado
    descripcion: "Cantina empresarial"
}
```

### Opción 2: Con logo (imagen)
```javascript
{
    nombre: "Empresa XYZ",
    sistema: "Vendora",
    logo: "imagenes/logo-xyz.png",  // O lo que sea tu ruta
    descripcion: "Tienda online de ropa"
}
```

### Opción 3: Sistemas con enlace
```javascript
{
    nombre: "Empresa XYZ",
    sistemas: [
        { nombre: "Vendora", url: "https://empresa.com/vendora" },
        { nombre: "Gestium" }
    ],
    logo: "imagenes/logo-xyz.png",
    descripcion: "Tienda online de ropa"
}
```

## Pasos:
1. **Abre** `index.html`
2. **Busca** `const clientsData = [`
3. **Copia** cualquier cliente existente como plantilla
4. **Pega** al final del array (antes del cierre)
5. **Modifica**: nombre, sistema, logo y descripción
6. **Guarda** y recarga la página

Si un sistema es privado, deja solo `{ nombre: "Sistema" }` sin `url`.

## Sistemas disponibles (atajos):
- ✅ MenuMaster
- ✅ Viandify
- ✅ Vitrino
- ✅ Vendora
- ✅ Vendora — Stock Control Plus
- ✅ Gestium

## Ejemplo completo para pegar:
```javascript
{
    nombre: "Tu Cliente Aquí",
    sistema: "MenuMaster",
    logo: "TC",
    descripcion: "Descripción del tipo de negocio"
}
```

## Notas:
- El **logo** se muestra como iniciales si solo pones 1-2 caracteres
- Puedes poner la ruta de una **imagen** si tienes logos en `imagenes/`
- La sección se actualiza automáticamente sin recargar código
- Los clientes tienen **animación** al entrar en vista

---
**¡Listo!** Solo copia el cliente que necesites y personaliza 🎉

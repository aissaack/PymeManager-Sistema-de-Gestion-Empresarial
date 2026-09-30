# Reglas del proyecto

## Calidad del código

- No generar código basura: nada de código muerto, comentado, duplicado, ni archivos o dependencias innecesarias.
- El código debe ser escalable, limpio, estructurado y legible.
- Nombres claros, responsabilidades separadas y funciones/componentes con un único propósito.

## Íconos

- No usar SVG.
- Usar etiquetas `<i />` con el `className` de Bootstrap Icons.

```jsx
<i className="bi bi-cart" />
```

## Decisiones y alcance

- No tomar decisiones de arquitectura ni de funcionalidades por cuenta propia.
- Si se quiere o requiere agregar algo nuevo que no esté definido en `.claude/spec.md`, se debe preguntar antes de hacerlo.

# Reporte de Errores - CSS

Al revisar el archivo `style.css` encontré tres fallas principales que impedían que la página se mostrara correctamente:

1. Falta de unidad en `width` (`width: 300`)
   CSS no sabe qué representan ese "300" (si píxeles, porcentajes, etc.), por lo que ignora la regla por completo. Lo corregí añadiéndole `px` (`width: 300px`).

2. Valor en español en `text-align` (`text-align: centro`) 
   Las propiedades de CSS solo entienden comandos en inglés. La palabra `centro` no es válida, así que la cambié por `center` (`text-align: center`).

3. Puntos y coma faltantes al final de algunas reglas  
   Hacían falta `;` al final de `font-family` en el selector `body` y de `border-style` en `.tarjeta-pokemon`. Sin ellos, el navegador se confunde al intentar leer la siguiente línea de código.

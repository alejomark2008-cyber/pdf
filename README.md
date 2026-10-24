# DIGIAR — Document Studio

Aplicación estática para edición local de PDF e imágenes. Diseño negro, blanco y plateado. Pie de página: Diseñado por Alejandro Romero.

## Publicación en GitHub + Vercel

1. Crea un repositorio nuevo en GitHub (por ejemplo, `DIGIAR`).
2. Sube `index.html`, `styles.css`, `app.js` y `README.md` a la raíz.
3. En Vercel selecciona **Add New → Project → Import Git Repository** y el repositorio.
4. Framework Preset: **Other**. No necesitas comando de build ni variables de entorno.
5. Pulsa Deploy. Vercel servirá `index.html` automáticamente.

Para pruebas locales, abre `index.html` en Chrome o usa `python -m http.server 8000` y visita `http://localhost:8000`.

## Herramientas incluidas

- Recorte masivo proporcional en PDF, hasta 100 páginas por archivo; mismo rectángulo relativo en todas las páginas. La región se configura mediante cajas de página PDF, por lo que algunos visores o herramientas pueden conservar contenido fuera del área visible internamente.
- Unir, dividir, extraer, eliminar, invertir, girar, numerar y marcar páginas.
- PDF a JPG/PNG, imágenes a PDF, conversión JPG/PNG/WebP, redimensionar y recortar imágenes en lote.
- Compresión de PDF por rasterización: **pierde texto seleccionable, enlaces y elementos vectoriales** y no siempre reduce el tamaño.

## Limitaciones de esta primera versión

- Los archivos se procesan localmente en el navegador. El rendimiento depende de la RAM del equipo; 100 páginas grandes pueden consumir mucha memoria.
- PDF con contraseña, formularios especiales, firmas digitales y documentos dañados pueden fallar. Editar un PDF invalida firmas digitales existentes.
- Para el recorte masivo, las páginas deben tener estructura y proporciones similares. No hay detección inteligente de objetos en esta versión.
- La herramienta «dividir» interpreta cada rango separado por coma como un PDF independiente.
- No hay OCR, conversión Word/PDF, firma digital, cifrado con contraseña ni eliminación de fondos. No se muestran como funciones disponibles.
- Las bibliotecas se cargan desde cdnjs; la primera visita necesita conexión a internet y el proveedor puede recibir datos técnicos de la conexión. No se envían los archivos a ese CDN.
- Antes de lanzamiento público: incorporar contacto legal y revisar la política de privacidad con la información real del responsable. Revisar dependencia CDN, CSP, accesibilidad y pruebas de archivos maliciosos.

## Dependencias

- PDF.js 3.11.174 (cdnjs)
- pdf-lib 1.17.1 (cdnjs)
- JSZip 3.10.1 (cdnjs)

Sin base de datos, sin cuentas, sin analítica y sin Supabase. Puedes añadirlo después con consentimiento informado y política de privacidad actualizada.

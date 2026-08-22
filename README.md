# legal-pages-soft-j

Páginas públicas de Política de Tratamiento de Datos, Términos y Condiciones, e instrucciones para eliminar cuenta, para las apps de Soft-J, publicadas con GitHub Pages. Repo público, **sin licencia** a propósito (todos los derechos reservados por default) — no es código abierto, es solo el hosting de documentos legales de apps privadas.

Vive **fuera** de los repos de las apps (Credit-J, Money J) a propósito: estas páginas son HTML/CSS 100% autocontenido, sin ningún import ni variable que dependa del código de ninguna app — no hay ninguna razón técnica para que compartan repo con ellas.

## Por qué existe

Google Play (y Apple, si algún día aplica) exige una URL pública de Política de Privacidad en la ficha de cada app. El código fuente de cada app es privado, así que estas páginas viven acá — separadas, públicas solo en lo que necesitan ser públicas.

## Estructura

Una carpeta por app, cada una con su propio `index.html` (política + términos) y `eliminar-cuenta.html`, autocontenidos (sin dependencias externas, mismo estilo visual y paleta de colores que la app correspondiente):

```
legal-pages-soft-j/
├── credit-j/
│   ├── index.html            → Política de Datos + Términos de Credit-J
│   └── eliminar-cuenta.html  → Instrucciones para eliminar cuenta y datos
└── money-j/
    ├── index.html            → Política de Datos + Términos de Money J
    └── eliminar-cuenta.html  → Instrucciones para eliminar cuenta y datos
```

## URLs publicadas

Con GitHub Pages activado (Settings → Pages → Deploy from a branch → `master` / `root`):

- Credit-J: `https://jjrr13.github.io/legal-pages-soft-j/credit-j/` · `.../credit-j/eliminar-cuenta.html`
- Money J: `https://jjrr13.github.io/legal-pages-soft-j/money-j/` · `.../money-j/eliminar-cuenta.html`

## Mantenimiento

El contenido real vive primero en el código de cada app (`src/constants/legalContent.js`, mostrado dentro de la app vía `LegalTextModal.js`). Estas páginas son una copia estática de ese mismo texto — si se edita `legalContent.js`, hay que reflejar el cambio acá también y volver a subir el `index.html` actualizado.

Money J, a diferencia de Credit-J, no maneja datos de terceros (sin clientes, sin organizaciones/equipos) — es de un solo usuario, así que su política es más corta (no incluye el rol de "Encargado del Tratamiento" frente a datos de otra persona) y su `eliminar-cuenta.html` no tiene la sección de "si sos cliente de un usuario de la app".

⚠️ Borrador funcional, no revisión legal — antes del lanzamiento real, que un abogado revise el contenido (Ley 1581 de 2012 / Habeas Data para el caso colombiano).

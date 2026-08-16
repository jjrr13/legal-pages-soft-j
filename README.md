# legal-pages-soft-j
Administracion de documentos publicos

Páginas públicas de Política de Tratamiento de Datos y Términos y Condiciones para las apps de Soft-J, publicadas con GitHub Pages. Repo público, **sin licencia** a propósito (todos los derechos reservados por default) — no es código abierto, es solo el hosting de documentos legales de apps privadas.

## Por qué existe

Google Play (y Apple, si algún día aplica) exige una URL pública de Política de Privacidad en la ficha de cada app. El código fuente de cada app es privado, así que estas páginas viven acá — separadas, públicas solo en lo que necesitan ser públicas.

## Estructura

Una carpeta por app, cada una con su propio `index.html` autocontenido (sin dependencias externas, mismo estilo visual que la app correspondiente):

```
legal-pages-soft-j/
├── credit-j/
│   └── index.html   → Política de Datos + Términos de Credit-J
└── money-j/          (se agrega cuando Money J lo necesite)
    └── index.html
```

## URLs publicadas

Con GitHub Pages activado (Settings → Pages → Deploy from a branch → `main` / `root`), cada carpeta queda disponible en:

- Credit-J: `https://<usuario>.github.io/legal-pages-soft-j/credit-j/`
- Money J: `https://<usuario>.github.io/legal-pages-soft-j/money-j/` (cuando exista)

## Mantenimiento

El contenido real vive primero en el código de cada app (Credit-J: `src/constants/legalContent.js`, mostrado dentro de la app vía `LegalTextModal.js`). Estas páginas son una copia estática de ese mismo texto — si se edita `legalContent.js`, hay que reflejar el cambio acá también y volver a subir el `index.html` actualizado.

⚠️ Borrador funcional, no revisión legal — antes del lanzamiento real, que un abogado revise el contenido (Ley 1581 de 2012 / Habeas Data para el caso colombiano).

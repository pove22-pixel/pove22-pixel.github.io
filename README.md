# HabilitadosNacionales.es — Guía de despliegue

Blog profesional sobre Habilitados Nacionales y Administración Pública Local.

---

## PASO 1 — Crear cuenta en GitHub (5 min)

1. Ve a **https://github.com** y haz clic en "Sign up"
2. Elige un nombre de usuario (por ejemplo: `habilitadosnacionales`)
3. Introduce tu email y una contraseña
4. Verifica tu cuenta con el email que recibirás

---

## PASO 2 — Crear el repositorio (3 min)

1. Una vez dentro de GitHub, haz clic en el botón verde **"New"** (arriba a la izquierda)
2. En "Repository name" escribe exactamente: `habilitadosnacionales.github.io`  
   *(sustituye `habilitadosnacionales` por tu nombre de usuario real)*
3. Marca la opción **"Public"**
4. Haz clic en **"Create repository"**

---

## PASO 3 — Subir los archivos (5 min)

1. En la página del repositorio recién creado, haz clic en **"uploading an existing file"**
2. Arrastra los dos archivos de esta carpeta:
   - `index.html`
   - `CNAME`
3. En el campo "Commit changes" escribe: `Sitio web inicial`
4. Haz clic en **"Commit changes"**

---

## PASO 4 — Activar GitHub Pages (2 min)

1. En el repositorio, haz clic en **"Settings"** (pestaña superior)
2. En el menú lateral izquierdo, haz clic en **"Pages"**
3. En "Source" selecciona **"Deploy from a branch"**
4. En "Branch" selecciona **"main"** y la carpeta **"/ (root)"**
5. Haz clic en **"Save"**

GitHub te mostrará: *"Your site is live at https://habilitadosnacionales.github.io"*

---

## PASO 5 — Configurar el dominio en IONOS (10 min)

Para que `www.habilitadosnacionales.es` apunte a GitHub Pages:

1. Entra en **my.ionos.es**
2. Ve a **Dominios & SSL** → selecciona `habilitadosnacionales.es`
3. Haz clic en la pestaña **"DNS"**
4. Añade o edita los siguientes registros:

### Registros A (para el dominio raíz sin www):
| Tipo | Nombre | Valor |
|------|--------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

### Registro CNAME (para www):
| Tipo | Nombre | Valor |
|------|--------|-------|
| CNAME | www | habilitadosnacionales.github.io |

*(Sustituye `habilitadosnacionales` por tu nombre de usuario real de GitHub)*

5. Guarda los cambios
6. Espera entre 30 minutos y 24 horas para la propagación DNS

---

## PASO 6 — Verificar el dominio en GitHub (2 min)

1. Vuelve a GitHub → Settings → Pages
2. En "Custom domain" escribe: `www.habilitadosnacionales.es`
3. Haz clic en **"Save"**
4. Marca la casilla **"Enforce HTTPS"** (puede tardar unos minutos en aparecer)

¡Listo! Tu web estará disponible en https://www.habilitadosnacionales.es

---

## Cómo publicar un artículo nuevo

1. Entra en **github.com** → tu repositorio
2. Haz clic en `index.html` → luego en el icono de lápiz (editar)
3. Busca la sección `const ARTICLES = [` al final del archivo
4. Copia y pega este bloque **al principio** de la lista (después del `[`):

```javascript
  {
    id: 31, slug: "titulo-del-articulo",
    title: "El título de tu nuevo artículo",
    cat: "Transformación Digital",  // o la categoría que corresponda
    date: "1 de abril, 2026", year: "2026", monthday: "1 abr",
    excerpt: "El primer párrafo o resumen del artículo en 1-2 frases.",
    wpUrl: "https://elnuevofuncionarioconhabilitaciondecaracternacional.wordpress.com/...",
    body: `<p>Aquí va el texto completo del artículo en HTML.</p>
           <p>Puedes usar etiquetas como <strong>negrita</strong>, <em>cursiva</em>.</p>
           <h2>Un subtítulo</h2>
           <p>Más texto...</p>`
  },
```

5. Haz clic en **"Commit changes"** → la web se actualiza en 1-2 minutos

---

## Categorías disponibles

- `Transformación Digital`
- `Habilitados Nacionales`
- `Recursos Humanos`
- `Contratación Pública`
- `Carrera Profesional`
- `Innovación`

---

## Soporte

Si algo no funciona, describe el paso exacto donde te quedas atascado
y Claude te ayudará a resolverlo.

# antoniojzaratel.com — Sitio personal

Revamp completo del sitio, reemplazando Google Sites. Un solo archivo (`index.html`, con CSS y JS incluidos), modo claro/oscuro, responsive (web y celular).

## Estructura

```
├── index.html              ← el sitio completo (HTML + CSS + JS en un solo archivo)
├── CNAME                    ← para conectar tu dominio en GitHub Pages
└── assets/
    ├── cv/CV_AntonioZarate.pdf   ← tu CV descargable (botón "Descargar CV")
    └── img/
        └── profile.jpg      ← ✅ ya incluida (tu foto)
```

## Publicarlo en 2 minutos (copiar y pegar)

Ya tu foto está incluida en `assets/img/profile.jpg`. Solo falta subirlo:

```bash
# 1. Crea un repo vacío en https://github.com/new
#    Nombre sugerido: antoniojzaratel.github.io  (usuario: antoniojzaratel)
#    NO lo inicialices con README

# 2. Desde la carpeta de este sitio:
git init
git add .
git commit -m "Sitio personal — revamp"
git branch -M main
git remote add origin https://github.com/antoniojzaratel/antoniojzaratel.github.io.git
git push -u origin main
```

Con ese nombre de repo (`antoniojzaratel.github.io`), GitHub Pages se activa automáticamente — no necesitas configurar nada en Settings → Pages.

## Cómo conectar tu dominio antoniojzaratel.com

Ya incluí el archivo `CNAME` con tu dominio, así que GitHub Pages lo reconocerá automáticamente. Falta apuntar tu dominio (donde lo compraste, ej. Google Domains/Squarespace, GoDaddy, etc.) hacia GitHub:

1. En el panel de DNS de tu proveedor de dominio, **elimina** los registros que apuntan a Google Sites.
2. Agrega estos registros **A** apuntando la raíz del dominio (`antoniojzaratel.com`) a las IPs de GitHub Pages:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
3. Agrega un registro **CNAME** para `www` apuntando a `antoniojzaratel.github.io`.
4. En GitHub, ve a **Settings → Pages → Custom domain**, escribe `antoniojzaratel.com` y guarda. Espera a que aparezca el check verde (puede tardar hasta 24h en propagar) y activa "Enforce HTTPS".

## Editar contenido más adelante

Todo el texto, fechas y links están directamente en `index.html` — puedes editarlo con cualquier editor de texto (o pedirme que lo actualice). Las secciones están comentadas y en el mismo orden que se ven en el sitio: Hero → Stats → Sobre mí → Experiencia → Skills → Proyectos → Educación → Contacto.

## Notas de diseño

- **Modo claro/oscuro**: botón en la barra de navegación (ícono sol/luna). Recuerda tu preferencia y respeta el modo del sistema operativo por defecto.
- **Responsive**: probado en escritorio y celular.
- **Accesible**: el contenido es visible incluso si JavaScript falla (no depende del scroll para aparecer), respeta "reduced motion", y tiene foco de teclado visible.
- Todas las cifras del sitio (POC de $350K+, roles, etc.) reflejan tu CV y LinkedIn ya actualizados — usa "retailer Fortune 500 con operación en México" en vez de nombrar al cliente directamente, tal como me pediste.

# Portfolio — Cáceres Ary Fernán

Portfolio personal de una sola página con Jekyll + Tailwind (CDN) + Leaflet, listo para GitHub Pages.

## Publicar en GitHub Pages

1. Crear repo (ej. `arieldelplata.github.io` o `portfolio`).
2. Subir estos archivos a la rama `main`.
3. En el repo: **Settings → Pages → Deploy from branch → `main` / `/ (root)`**.
4. Abrir `https://<usuario>.github.io/` (o `/portfolio/` si no es repo de usuario).

> Si el repo NO es `<usuario>.github.io`, Jekyll usa `baseurl`. Ajustá `_config.yml`:
> `url: "https://arieldelplata.github.io"` y `baseurl: "/portfolio"`.

## Personalizar

- **Foto:** reemplazá `assets/img/foto-perfil.jpg` (ideal 800×800). El `<img>` tiene fallback a placeholder si no existe.
- **Certificado IGCSE:** reemplazá `assets/docs/certificado-igcse.pdf` con el real (mismo nombre para no tocar el link).
- **Proyectos:** en `index.html`, sección `#proyectos`, duplicá una `<article>` del grid.
- **Cursos:** en `#educacion`, completá las 2 tarjetas placeholder (título, institución, link de credencial).
- **Áreas / skills:** badges en `#intereses` y `<li>` en `#habilidades`, duplicables.
- **Idioma:** toggle en navbar + botón flotante. Todo texto duplicado con clases `.lang-es` / `.lang-en`, sin recarga (JS vanilla + `localStorage`).

## Desarrollo local

```powershell
gem install bundler jekyll
bundle install
bundle exec jekyll serve
# abrir http://localhost:4000
```

## Estructura

```text
_config.yml  Gemfile  index.html
_layouts/default.html
_includes/navbar.html  _includes/footer.html
assets/img/foto-perfil.jpg  assets/docs/certificado-igcse.pdf
```

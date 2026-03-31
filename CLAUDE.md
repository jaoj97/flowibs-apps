# FLOW IBS Apps — Web Apps Platform

## Proyecto
Plataforma de apps web estáticas hosteadas en GitHub Pages.
- **URL producción:** https://apps.flowibs.com
- **Repo:** https://github.com/jaoj97/flowibs-apps
- **Hosting:** GitHub Pages con custom domain (GoDaddy DNS)

## Estructura
```
flowibs-apps/
├── index.html              ← Landing page protegida con contraseña
├── CNAME                   ← Custom domain (apps.flowibs.com)
├── flowbrand/index.html    ← Brand Kit Visualizer app
└── [future-app]/index.html ← Futuras apps van en su propia carpeta
```

## Deployment
Para hacer deployment, ejecutar:
```bash
cd ~/Projects/flowibs-apps
git add .
git commit -m "descripción del cambio"
git push origin main
```
GitHub Pages se actualiza automáticamente en ~1-2 minutos tras el push.

## Rollback (regresar a versión anterior)
- Ver historial: `git log --oneline`
- Revertir último cambio: `git revert HEAD && git push origin main`
- Revertir commit específico: `git revert <hash> && git push origin main`

## Agregar nueva app
1. Crear carpeta: `mkdir ~/Projects/flowibs-apps/nombre-app`
2. Crear `index.html` dentro
3. Agregar card en `index.html` raíz (landing page)
4. Deploy normalmente

## Notas importantes
- La landing page (`index.html` raíz) está protegida con contraseña JavaScript
- Las apps individuales son accesibles directamente por URL sin contraseña
- Cada app vive en su propia carpeta con su propio `index.html`
- No subir archivos .env ni credenciales al repo

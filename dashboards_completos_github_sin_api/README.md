# Dashboards de transporte de carga

Contenido listo para publicar en GitHub Pages directamente desde `main` y `/ (root)`:

- `index.html`: página de inicio con enlaces a los tres mapas.
- `Generación.html`: generación de carga.
- `Atraccion_ajustada.html`: atracción ajustada.
- `Patentes_Entregas.html`: patentes y entregas.
- `.nojekyll`: desactiva el procesamiento de Jekyll.

## Publicación

Extrae el ZIP y copia **todos los archivos**, incluido `.nojekyll`, a la carpeta local que ya está conectada al repositorio GitHub `dashboards`. Luego ejecuta desde esa carpeta:

```bash
git add .
git commit -m "Actualizar dashboards con mapa base sin API"
git push origin main
```

En GitHub, mantén `Settings → Pages → Deploy from a branch → main → / (root)`.

Página principal esperada: `https://rodrigommelendez.github.io/dashboards/`

## Mapa base

La cartografía se sirve con teselas estándares de OpenStreetMap (`https://tile.openstreetmap.org/{z}/{x}/{y}.png`) mediante MapLibre, **sin API key ni cuenta**. Se muestra la atribución a OpenStreetMap en el mapa.

Los datos H3 están **incorporados** en los propios HTML; no necesitas subir bases `.pkl`, `.xlsx` ni `.geojson`.

Se necesita Internet para las teselas y las bibliotecas JavaScript cargadas desde CDN. El servidor gratuito de OpenStreetMap tiene una política de uso y no garantiza disponibilidad ilimitada. Es apropiado para consultas interactivas de tráfico moderado, no para descarga masiva de mapas: https://operations.osmfoundation.org/policies/tiles/.

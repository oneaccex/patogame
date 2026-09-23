# patogame

Publica **https://patogame.oneaccex.com** a partir de [anfcadavidag/patogame](https://github.com/anfcadavidag/patogame).

- `publicar` corre cada ~5 min: si hay un tag nuevo en el repo de Andrés, copia sus archivos (no ejecuta nada) al bucket S3 y refresca CloudFront. `VERSION` dice qué está publicado.
- Volver atrás: Actions → publicar → Run workflow → escribir el tag (ej. `v1.1`).
- `mantener-vivo` hace un commit mensual para que GitHub no apague el chequeo programado.
- Infra: `infra/patogame.tf` en oneaccex/oneaccex. El rol de AWS solo acepta la rama `main` de este repo y solo puede escribir en ese bucket.

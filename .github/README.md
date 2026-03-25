# Ejemplo de anidacion de workflows reusables (GitHub Actions)

Esta carpeta contiene un ejemplo minimo de **anidacion** de workflows reusables:

1. `caller-nested-example.yml` (workflow principal)
2. `reusable-level-1.yml` (workflow reusable de nivel 1)
3. `reusable-level-2.yml` (workflow reusable de nivel 2)

Flujo:

- El workflow principal llama al reusable de nivel 1.
- El reusable de nivel 1 llama al reusable de nivel 2.
- El reusable de nivel 2 genera un output (`artifact_name`) que se propaga hacia arriba.

Para probarlo:

1. Haz push de estos archivos al repositorio.
2. Ve a **Actions** en GitHub.
3. Ejecuta manualmente `Caller - Nested Reusable Workflow Example`.
4. Revisa los logs del job `show-final-output` para ver el output final.

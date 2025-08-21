# Teoría básica de Git (Resumen para la práctica)

## ¿Qué es Git?
Git es un **sistema de control de versiones distribuido** que registra cambios en archivos a lo largo del tiempo y facilita el trabajo en equipo.

## Conceptos clave
- **Repositorio (repo):** carpeta con historial de cambios. Puede ser **local** (tu PC) o **remoto** (GitHub).
- **Working Directory:** tus archivos editables.
- **Staging Area (index):** zona intermedia donde preparas qué va a entrar al commit.
- **Commit:** captura (snapshot) de los cambios con un mensaje.
- **Rama (branch):** línea de tiempo independiente para desarrollar en paralelo.
- **Remoto (origin):** nombre habitual para el repo en GitHub.
- **HEAD:** apunta a tu commit/rama actual.

## Flujo mínimo
1. Editas archivos → `git status` y `git diff`
2. Preparas cambios → `git add <archivo>`
3. Confirmas cambios → `git commit -m "mensaje"`
4. Envías al remoto → `git push origin <rama>`
5. Traes cambios del remoto → `git pull` (o `git pull --rebase`)

## Ramas en breve
- Crear rama: `git switch -c mi-rama` (o `git checkout -b mi-rama`)
- Cambiar de rama: `git switch main`
- Unir ramas: `git merge mi-rama` (desde `main`), o rebase: `git rebase main`

## Buenas prácticas de mensajes de commit
- Imperativo: “Agrega validación de email”
- Breve (<= 72 caracteres) y claro
- Un commit por idea/cambio

## Colaboración
- Sincroniza seguido: `git pull --rebase origin main`
- Evita editar archivos de otros compañeros
- Resuelve conflictos con calma: edita, `git add`, continúa

## GitHub (remoto)
- Aloja repositorios y facilita revisión de cambios
- *Pull Request (PR):* propuesta de cambios para revisión (no se usa en la práctica mínima, pero es útil)


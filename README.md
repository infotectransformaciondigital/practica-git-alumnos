# Práctica GIT – Edición de tu página (Proyecto de aula)

Este repositorio contiene **index.html** y una carpeta **src/** con un archivo HTML por estudiante.
Tu tarea es **editar solo tu archivo** y subir los cambios mediante Git.

## Objetivos
- Clonar un repositorio remoto
- Editar un archivo y registrarlo en el *staging area*
- Crear un *commit* con mensaje significativo
- Enviar los cambios al remoto (*push*) y verificar

## Requisitos previos
- Git instalado (`git --version`)
- Editor de texto (VS Code recomendado)
- Usuario de GitHub con acceso al repo

---

## Pasos rápidos (CLI)
> Si prefieres interfaz gráfica, hay una guía al final.

1. **Clonar el repo**
```bash
git clone <URL_DEL_REPO>
cd practica-git-alumnos   # o el nombre real del repo
```

2. **Configurar tu identidad (una sola vez en tu PC)**
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

3. **Editar SOLAMENTE tu archivo en `src/`**
   - Abre `index.html` para ubicar tu nombre y el archivo asignado.
   - Edita tu archivo dentro de `src/` y guarda.

4. **Revisar cambios**
```bash
git status
git diff  # opcional, para ver qué cambió
```

5. **Preparar y confirmar**
```bash
git add src/tu_archivo.html
git commit -m "Actualizo mi página personal (Tu Nombre)"
```

6. **Enviar al remoto**
```bash
git push origin main
```
> Si el repo usa otra rama (p. ej. `master`), reemplaza `main` por `master`.

7. **Verificar**
- Actualiza la página del repo en GitHub y confirma que tu commit aparece en *History*.
- Abre `index.html` en tu navegador local para validar tu cambio.

---

## Notas y buenas prácticas
- Trabaja **únicamente** en tu archivo. No edites el de otra persona ni `index.html`.
- Mensajes de commit: cortos, claros y en infinitivo.
- Si ocurre un error de *non-fast-forward* o *rejected*:
  ```bash
  git pull --rebase origin main
  git push origin main
  ```
- Si aparece un **conflicto**, edita el archivo para resolverlo, guarda, y:
  ```bash
  git add <archivo>
  git rebase --continue    # si estabas en rebase
  git push origin main
  ```

---

## Uso con VS Code (GUI)
1. Abre la carpeta del repo en VS Code.
2. Cambia tu archivo en `src/` y guarda.
3. Ve a la pestaña **Source Control** (icono de rama).
4. Revisa los cambios, escribe el mensaje de commit y presiona **Commit**.
5. Haz clic en **Sync Changes** o **Push**.

---

## Entregable
- 1 commit que modifique **solo** tu archivo.
- Tu archivo debe incluir:
  - Tu nombre completo y matrícula (si aplica).
  - Un breve párrafo de presentación.
  - (Opcional) Una imagen y enlaces.

---

## Evaluación sugerida
- 40%: Flujo Git correcto (add/commit/push, mensaje claro).
- 40%: Contenido y formato de la página personal.
- 20%: Buenas prácticas (solo su archivo, sin conflictos innecesarios).

---

## Apéndices
- Consulta `TEORIA_GIT_RESUMEN.md` y `GIT_CHEATSHEET.md` para teoría y atajos.
- Problemas comunes y soluciones rápidas están en el *cheatsheet*.

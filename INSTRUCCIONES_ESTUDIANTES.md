# Instrucciones para Estudiantes – Práctica GIT

## Contexto
El repositorio contiene una página principal `index.html` y una carpeta `src/` con un archivo para cada estudiante. Debes **editar únicamente el archivo que corresponde a tu nombre** y subir los cambios con Git.

## 1) Preparación
- Verifica que Git esté instalado: `git --version`.
- Configura tu identidad (solo la primera vez en tu equipo):
  ```bash
  git config --global user.name "Tu Nombre"
  git config --global user.email "tu@email.com"
  ```

## 2) Clonar el repositorio
```bash
git clone <URL_DEL_REPO>
cd <carpeta_del_repo>
```

## 3) Ubicar tu archivo
- Abre `index.html` para ver la lista de nombres/enlaces.
- Localiza tu archivo dentro de `src/` (ejemplo: `juan_perez_lopez.html`).

## 4) Editar tu página
- Abre tu archivo en un editor (VS Code recomendado).
- Añade: nombre completo, matrícula (si aplica) y un breve párrafo de presentación.
- Guarda.

## 5) Crear tu commit
```bash
git status                 # ver cambios
git add src/mi_archivo.html
git commit -m "Actualizo mi página personal (Tu Nombre)"
```

## 6) Subir al remoto
```bash
git push origin main
```
> Si la rama por defecto es `master`, usa `master`.

## 7) Validar
- En GitHub, revisa el historial de commits.
- Asegúrate de que tu archivo fue el único modificado.

---

## Reglas
- **Edita solo tu archivo**.
- No cambies `index.html` ni archivos de otros compañeros.
- Mensajes de commit breves y descriptivos.

## Puntos extra (opcional)
- Usa listas, enlaces o una imagen en tu HTML.
- Corrige tu commit si el docente te lo pide:
  ```bash
  # haces cambios
  git add src/mi_archivo.html
  git commit -m "Mejora de contenido (Tu Nombre)"
  git push origin main
  ```

## Soporte rápido
- Error *rejected*: ejecuta `git pull --rebase origin main` y luego `git push`.
- Error de permisos: verifica que usas el **mismo** usuario de GitHub que tiene acceso.
- Conflictos: abre el archivo, busca `<<<<<<<` y `>>>>>>>`, resuelve, `git add`, y continúa.

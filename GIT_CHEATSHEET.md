# Git Cheatsheet (atajos y problemas comunes)

## Comandos frecuentes
- Estado: `git status`
- Ver diferencias: `git diff`
- Agregar cambios: `git add <archivo>` o `git add .`
- Confirmar: `git commit -m "mensaje"`
- Enviar: `git push origin main`
- Traer: `git pull --rebase origin main`
- Log simple: `git log --oneline --graph --decorate --all`

## Configuración básica (una vez)
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

## Ramas
```bash
git switch -c feature-x      # crear y cambiar
git switch main              # volver a main
git merge feature-x          # unir (desde main)
```

## Errores típicos y soluciones
- **rejected (non-fast-forward)**  
  Tu rama local está desactualizada.
  ```bash
  git pull --rebase origin main
  git push origin main
  ```

- **Permission denied** (HTTPS)  
  Revisa las credenciales de GitHub o usa un token personal.

- **Conflictos de merge/rebase**  
  Edita los archivos marcados, guarda y:
  ```bash
  git add <archivo_resuelto>
  git rebase --continue   # si estabas en rebase
  # o git merge --continue si estabas en merge
  git push origin main
  ```

- **Quiero deshacer mi último commit (sin perder cambios)**  
  ```bash
  git reset --soft HEAD~1
  ```

- **Quiero descartar cambios sin comprometer**  
  ```bash
  git checkout -- <archivo>
  ```

## Consejos
- Haz commits pequeños y frecuentes.
- Escribe mensajes claros.
- Sincroniza antes de empezar a trabajar: `git pull --rebase`.

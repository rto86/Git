___

# 1. Instalación y verificación de Git

Antes de usar Git Bash, asegúrate de tener Git instalado.

### ✔️ Verificar si Git está instalado


```bash
git --version
```

Si aparece un número de versión, Git está instalado.

### ✔️ Si no está instalado

Descárgalo desde la web oficial: _git-scm.com_ (Windows, macOS, Linux). Durante la instalación en Windows, selecciona **Git Bash** como terminal predeterminada.

# 2. Configuración inicial de Git (obligatoria)

Git necesita saber quién eres para registrar tus cambios.

### ✔️ Configurar nombre y correo (global)


```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
```

### ✔️ Ver configuración actual


```bash
git config --global --list
```

### ✔️ Configurar editor por defecto (opcional)


```bash
git config --global core.editor "code --wait"
```

# 3. Crear tu primer repositorio

### ✔️ Crear carpeta del proyecto

```bash
mkdir mi-proyecto
cd mi-proyecto
```

### ✔️ Inicializar Git


```bash
git init
```

Esto crea la carpeta oculta `.git` donde Git guarda todo el historial.

# 4. Estados de Git: el corazón del sistema

Git trabaja con **tres estados**:

- **Working Directory** → donde editas archivos
    
- **Staging Area** → preparación antes del commit
    
- **Repository (History)** → historial permanente
    

# 5. Comandos esenciales del día a día

### Ver el estado del repositorio


```bash
git status
```

### Añadir archivos al staging

- Un archivo:
    

```bash
git add archivo.txt
```

- Todos los archivos:
    

```bash
git add .
```

### 📌 Crear un commit


```bash
git commit -m "Descripción del cambio"
```

### 📌 Ver historial de commits


```bash
git log
```

### 📌 Ver diferencias antes del commit


```bash
git diff
```

#  6. Trabajar con archivos

### 📌 Renombrar archivos


```bash
git mv viejo.txt nuevo.txt
```

### 📌 Eliminar archivos


```bash
git rm archivo.txt
```

### 📌 Recuperar archivo modificado


```bash
git restore archivo.txt
```

### 📌 Recuperar archivo eliminado


```bash
git restore --staged archivo.txt
```

#  7. Ramas (branches): trabajo paralelo

### 📌 Crear una rama

```
git branch nueva-rama
```

### 📌 Cambiar de rama

```bash
git checkout nueva-rama
```

o el comando moderno:

```bash
git switch nueva-rama
```

### 📌 Crear y cambiar a la vez

```bash
git checkout -b feature-login
```

### 📌 Ver ramas

```bash
git branch
```

## 📌 Fusionar ramas (merge)

Primero ve a la rama donde quieres fusionar:

```bash
git checkout main
git merge feature-login
```

### 📌 Eliminar rama

```bash
git branch -d feature-login
```

#  8. Conectar con GitHub (repositorio remoto)

### 📌 Añadir un remoto


```bash
git remote add origin https://github.com/usuario/repositorio.git
```

### 📌 Subir cambios


```bash
git push -u origin main
```

### 📌 Descargar cambios del remoto


```bash
git pull
```

### 📌 Clonar un repositorio existente


```bash
git clone https://github.com/usuario/repositorio.git
```

#  9. Archivo .gitignore

Sirve para excluir archivos que **no deben versionarse** (logs, node_modules, .env…).

Ejemplo:

```bash
node_modules/
.env
*.log
```

# 10. Comandos avanzados muy útiles

### 📌 Guardar cambios temporalmente (stash)

```bash
git stash
git stash pop
```

### 📌 Reescribir historial (rebase)

```bash
git rebase main
```

### 📌 Buscar errores entre commits (bisect)

```bash
git bisect start
```

### 📌 Ver un commit específico

```bash
git show 3f2a1c
```

# 11. Flujo de trabajo recomendado (Git Flow básico)

1. `main` → rama estable
    
2. `develop` → rama de desarrollo
    
3. `feature/*` → nuevas funcionalidades
    
4. `hotfix/*` → arreglos urgentes
    
5. Merge a `main` solo cuando esté probado
    

# 12. Ejemplo completo de flujo real

### 1. Crear proyecto


```bash
mkdir tienda
cd tienda
git init
```

### 2. Crear archivo


```bash
echo "<h1>Tienda</h1>" > index.html
git add index.html
git commit -m "Primer commit"
```

### 3. Crear rama de funcionalidad


```bash
git checkout -b feature-carrito
```

### 4. Editar archivo


```bash
echo "<p>Carrito</p>" >> index.html
git add .
git commit -m "Añadido carrito"
```

### 5. Volver a main y fusionar


```bash
git checkout main
git merge feature-carrito
```

## Mapa mental

<img width="1536" height="1024" alt="imagen" src="https://github.com/user-attachments/assets/05080bd1-01cf-42b9-9b0a-f29337218b1e" />



## Diagrama de flujo

<img width="1024" height="1536" alt="imagen" src="https://github.com/user-attachments/assets/c1193746-091b-4b16-ba50-353c677f7138" />


## Infografía

<img width="1024" height="1536" alt="imagen" src="https://github.com/user-attachments/assets/5a5dffcb-c274-43c5-a974-9e4c923e6151" />





# GuiaGit
¡Perfecto! Aquí tienes una guía paso a paso para trabajar con Anaconda Prompt y Git para subir y actualizar un repositorio desde cero:

### Configuración Inicial

**Instalación de Git**:
Si aún no has instalado Git, puedes obtenerlo desde el sitio web oficial de Git (https://git-scm.com/).

**Configuración de Git**:
Antes de usar Git, debes configurarlo con tu nombre de usuario y correo electrónico. Abre Anaconda Prompt y escribe:
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
```

### Crear un Nuevo Repositorio en GitHub

1. **Ir a GitHub** y hacer clic en el ícono "+" en la esquina superior derecha, luego en "New repository".

2. **Rellenar la información** necesaria para tu nuevo repositorio, como el nombre, descripción, visibilidad, etc.

3. **Crear el repositorio** haciendo clic en "Create repository".

### Subir el Repositorio Local desde cero

1. **Crear una Carpeta Nueva** para tu proyecto en tu máquina local.
   ```bash
   mkdir NombreDeTuProyecto
   cd NombreDeTuProyecto
   ```

2. **Inicializar el Repositorio Local** de Git.
   ```bash
   git init
   ```

3. **Añadir Archivos**. Crea un nuevo archivo o añade archivos existentes a tu carpeta.
   ```bash
   git add .
   ```

4. **Primer Commit**. Registra los cambios en el repositorio con un mensaje descriptivo.
   ```bash
   git commit -m "Primer commit con los archivos del proyecto"
   ```

5. **Conectar con el Repositorio Remoto**.
   ```bash
   git remote add origin URL_DEL_REPOSITORIO_GITHUB
   ```
   Reemplaza `URL_DEL_REPOSITORIO_GITHUB` con la URL que te proporciona GitHub.

6. **Subir al Repositorio Remoto**.
   ```bash
   git push -u origin main
   ```
   Usa `main` como el nombre de la rama si es la rama principal. Si tu rama se llama de otra manera, reemplázalo con el nombre correcto.

### Actualizar un Archivo

1. **Hacer Cambios**. Modifica el archivo que necesitas actualizar con tu editor de texto o IDE favorito.

2. **Agregar los Cambios** al área de preparación.
   ```bash
   git add archivo_modificado.txt
   ```

3. **Crear un Nuevo Commit** con estos cambios.
   ```bash
   git commit -m "Actualizado archivo_modificado.txt con nuevos datos"
   ```

4. **Subir los Cambios** al repositorio remoto.
   ```bash
   git push origin main
   ```

### Tips Importantes

- **Verificar el Estado**: Puedes verificar el estado de tu repositorio local con `git status`.
  
- **Historial de Commits**: Para ver tu historial de commits, utiliza `git log`.
  
- **Ignorar Archivos**: Si hay archivos que no quieres subir a GitHub (por ejemplo, archivos de configuración personal, contraseñas, etc.), puedes añadirlos a un archivo `.gitignore`.

- **Pull Antes de Push**: Siempre haz `git pull` antes de `git push` para asegurarte de que tu repositorio local esté sincronizado con el remoto.

- **Conflictos**: Si tienes conflictos al hacer `git pull`, deberás resolverlos antes de poder hacer un commit y push.

- **Anaconda Environments**: Si estás usando Anaconda y quieres compartir tu entorno, puedes exportar tu entorno con `conda env export > environment.yml` y luego añadir `environment.yml` a tu repositorio.

Recuerda que trabajar con repositorios Git es un ciclo constante de hacer cambios, hacer commits y subir esos cambios al repositorio remoto. Con el tiempo y práctica, este proceso se volverá una segunda naturaleza.

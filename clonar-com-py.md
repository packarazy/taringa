A continuación te doy un código en Python que clona un repositorio usando la dirección almacenada en una variable, y que lo clona en la misma carpeta desde donde se ejecuta el script:

✅ Código:

import git
import os

# Dirección del repositorio que deseas clonar
repo_url = "https://github.com/usuario/repositorio.git"

# Obtener el nombre del repositorio a partir de la URL
repo_name = repo_url.rstrip("/").split("/")[-1].replace(".git", "")

# Directorio actual (donde se ejecuta el script)
current_dir = os.getcwd()

# Ruta de destino donde se clonará el repositorio
clone_path = os.path.join(current_dir, repo_name)

# Clonar el repositorio
try:
    git.Repo.clone_from(repo_url, clone_path)
    print(f"Repositorio clonado exitosamente en: {clone_path}")
except Exception as e:
    print(f"Error al clonar el repositorio: {e}")

🔧 Requisitos:

Instala GitPython si no lo tienes:

pip install gitpython

📝 Notas:

El script extrae automáticamente el nombre del repositorio desde la URL (repositorio.git → repositorio) para usarlo como nombre de carpeta.

El repositorio se clonará en la misma carpeta donde está ubicado el archivo .py.


¿Quieres que agregue soporte para repositorios privados con autenticación también?


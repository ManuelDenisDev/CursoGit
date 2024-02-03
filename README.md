#

# Guia Markdown

---

#

### CursoGit by Manu Rodríguez [@manucondin](https://github.com/manucodin/manucodin)

Tutorial gratuito sobre Git - Git desde 0! [Ir al curso](https://www.udemy.com/course/git-desde-cero/)

#

---

### Instalacion

---

```
$ apt-get install git

$ git -v
$ git --version
```

#

---

### Configuracion

---

```
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com

$ git config user.name
John Doe

$ git config user.email
johndoe@example.com

$ git config --global init.defaultBranch main

$ git config --list
user.name=ManuelDenisDev
user.email=manueldenis.developer@gmail.com
init.defaultbranch=main

```

#

---

### Comandos basicos

---

| Accion                                    | Comando                                                                        |
| ----------------------------------------- | ------------------------------------------------------------------------------ |
| **Crear Repositorios:**                   | `$ git init`                                                                   |
| **Estado del repositorio:**               | `$git status`                                                                  |
| **Añadiendo al Starting Area:**           | `$git add .` / `$git add <archivo>`                                            |
| **Comitear archivos:**                    | `$git commit -am "Mensaje a comitear"` / `$git commit -m "Mensaje a comitear"` |
| **Consultar ramas:**                      | `$git branch`                                                                  |
| **Crear y cambiar de rama:**              | `$git checkout -b <nombre>`                                                    |
| **Cambiar de rama:**                      | `$git checkout <nombre>`                                                       |
| **Unir main con otra rama (desde main):** | `$git merge <rama> <nombre>`                                                   |
| **Eliminar rama:**                        | `$git branch -d <nombre>` / `$git branch -D <nombre>`                          |

#

---

### GitHub

---

Sitio web oficial de GitHub: [GitHub](https://github.com/)

Conectar a GitHub con CLAVE SSH [Documentacion oficial](https://docs.github.com/es/authentication/connecting-to-github-with-ssh)

#

---

## Generar una nueva clave SSH

---

-   Linux:
    -   Abre el Terminal.
    -   `$ ssh-keygen -t ed25519 -C "your_email@example.com"`
    -   `> Enter a file in which to save the key (/home/YOU/.ssh/id_ALGORITHM):[Press enter]`
    -   `> Enter passphrase (empty for no passphrase): [Type a passphrase]`
    -   `> Enter same passphrase again: [Type passphrase again]`

#

---

### Agregar tu clave SSH al ssh-agent

---

-   Linux:
    -   `$ eval "$(ssh-agent -s)"`
    -   `> Agent pid 59566`
    -   reemplaza \_id_ed25519 en el comando por el nombre de tu archivo de clave privada.
    -   `ssh-add ~/.ssh/id_ed25519`

![Imagen de github](./img/Captura%20de%20pantalla%202024-02-03%20152754.png)

#

---

### Crear repositorios remotos

---

Puede usar el comando `git remote add` para comparar una dirección URL remota con un nombre. Por ejemplo, escribirás lo siguiente en la línea de comandos:

```
git remote add origin <REMOTE_URL>
```

Esto asocia el nombre `origin` a `REMOTE_URL`.

Puede usar el comando `git remote set-url` para cambiar la dirección URL de un repositorio remoto.

#

---

### Agregar un repositorio remoto

---

-   Linux:

Para agregar un repositorio remoto nuevo, use el comando `git remote add` en el terminal, dentro del directorio donde está almacenado su repositorio.

El comando `git remote add` toma dos argumentos:

-   Un nombre remoto, por ejemplo, origin
-   Una dirección URL remota, por ejemplo, https://github.com/OWNER/REPOSITORY.git

Por ejemplo:

```
$ git remote add origin https://github.com/OWNER/REPOSITORY.git
# Set a new remote

$ git remote -v
# Verify new remote
> origin  https://github.com/OWNER/REPOSITORY.git (fetch)
> origin  https://github.com/OWNER/REPOSITORY.git (push)
```

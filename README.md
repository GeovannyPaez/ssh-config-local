# Como configurar llave SSH en cualquier Sistema Operativo
## Generar una nueva llave SSH: (Cualquier sistema operativo)

 ```bash 
 $ ssh-keygen -t rsa -b 4096 -C "youremail@example.com"
 ```

Comprobar proceso y agregarlo (Windows)
 ```bash 
eval $(ssh-agent - s)
 ```
  ```bash 
ssh-add ~/.ssh/id_rsa
 ```
 Comprobar proceso y agregarlo (Linux)
 ```bash 
eval "$(ssh-agent -s)"
 ```
  ```bash 
ssh-add ~/.ssh/id_rsa
 ```
Comprobar proceso y agregarlo (Mac)
  ```bash 
eval "$(ssh-agent -s)"

 ```

¿Usas macOS Sierra 10.12.2 o superior?
Haz lo siguiente:
  ```bash 
cd ~/.ssh

 ```

Crea un archivo config…
Con Vim vim config
Con VSCode code config
Pega la siguiente configuración en el archivo…
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_rsa
Agrega tu llave

  ```bash 
ssh-add -K ~/.ssh/id_rsa

 ```

🥳

# parcial1
Juan Sebastián Valencia Charry		2205254
Andrés David Luna Peña 						2184984


Denegar usuarios con PAM y pam_listfile
1. Instalación módulo:
Asegúrate de tener instalado el módulo pam_listfile
Apt get update

Apt-get- install apache2 libapache2-mod-authnz-pam


2. Crear archivo de lista:
Crea un archivo con la lista de usuarios denegados (/etc/pam.d/deny_users.txt):

usuario1
usuario2
...


3. Configuración de los módulos PAM y configuración de los Denegados:

auth required 			pam_unix.so 
account required 		pam_unix.so 
auth required 			pam_listfile.so onerr=fail 
item=user sense=deny
file=/etc/apache2/denegados.txt

4. Habilitación página:

a2dissite 000-default.conf 			Deshabilita
a2ensite 0oo-default.conf 			Habilita

5. Configuración de Apache: 
Edita el archivo de configuración de Apache para habilitar la autenticación y autorización PAM. Esto se hace mediante la configuración del archivo 000-default.conf o cualquier archivo de configuración relevante para tu sitio web en /etc/apache2/sites-available/.
6.Restart al apache:
Hacemos el restart con systemctl Restart apache2 para poder guardar los cambios realizados a este mismo.
7. Instalación del túnel:
A continuación, podremos ver los pasos a seguir para instalar correctamente el túnel.
Pasos:
1. Registrarte en ngrok
2. Selección Linux

3. Utilizamos el código brindado por el servidor para la instalación de nrgok
curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc \
| sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null && echo "deb https://ngrok-agent.s3.amazonaws.com buster main" \
| sudo tee /etc/apt/sources.list.d/ngrok.list && sudo apt update && sudo apt install ngrok
4. utilizando el comando:
sudo negrok http 192.168.50.3
obtenemos el link 
https://5d1e-45-5-189-189.ngrok-free.app

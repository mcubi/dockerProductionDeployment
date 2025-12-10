# GENERAL DOCUMENTATION OF THIS PROCESS (IT WILL BE BRIEF CAUSE OF I'M LATE)
## FIRST PART: DEV STAGE.
### For this primal stage we must dockerize the application in some parts as a dev environment. For that I will be using 'Docker Compose' -> [ .yaml and dockerfile ]
### dockerfile: 
<img width="778" height="317" alt="image" src="https://github.com/user-attachments/assets/82b592f3-350e-445f-bf27-08e8b410df93" />

### .yaml:
<img width="1042" height="399" alt="image" src="https://github.com/user-attachments/assets/63fed4c9-0af8-40c3-9c68-d35665e0ca72" />

### The list of the requirements was missing in the original project, so I had to create it:
<img width="474" height="215" alt="image" src="https://github.com/user-attachments/assets/d7920eb6-11e4-4714-b354-f9d9bdc6d46d" />

### End of the DEV STAGE!.

## SECOND PART: STAGE 1.
### For good practise, we must disable / eliminate the Django automatic browser reloading. So, we must eliminate reload urls included and remove it from the installed apps and middlewares:

<img width="950" height="566" alt="Captura de pantalla 2025-12-10 111456" src="https://github.com/user-attachments/assets/4b85d20e-d87c-43d8-ad0b-557a0023ada4" />

<img width="1130" height="648" alt="reloadsettings" src="https://github.com/user-attachments/assets/72d58e43-66e4-4d8b-b47c-a932c0d6fd46" />

### If you do not want to install it, remove it too from requirements.txt

### Then, we must adapt the commands of the dockerfile so we start the listening of the wsgi

<img width="938" height="301" alt="Captura de pantalla 2025-12-10 112105" src="https://github.com/user-attachments/assets/056238b2-62ac-445c-85f0-30d0abb90a52" />

### Looking in wsgi you might find the reload also there, but in my case it wasn't like that so I didn't have to remove it

### End of STAGE 1!

## LAST PART: STAGE 2.

### First, I created the nginx server configuration:

<img width="1527" height="725" alt="nginx" src="https://github.com/user-attachments/assets/76016393-d4c9-42dd-bfe3-a2b64b0fbbe7" />

### Then I moddified the Compose.yaml so i include the server and let it the exit of the information, so the web sercvice only exposses it's port. Also I built the volumes, and chnaged the default command

<img width="1127" height="811" alt="image" src="https://github.com/user-attachments/assets/63f5c33c-9076-4294-b096-7134d358f827" />

### Third, I moddified settings.py to add the staticfiles path

<img width="927" height="427" alt="set2" src="https://github.com/user-attachments/assets/eea1e2bb-4339-4d4c-84fd-2f44bb1a22b6" />

### Finally, I added gunicorn to the requirements list

<img width="762" height="247" alt="req2222222" src="https://github.com/user-attachments/assets/c808a0e7-4e12-4efc-bf89-1c51da9769a2" />

### End of the practise






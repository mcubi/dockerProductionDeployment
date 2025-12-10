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



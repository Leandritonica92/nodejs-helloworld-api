# NodeJs, helloworld API for test propouses.

This is a simple API that returns a welcome message.

## Run your local environment

### Clone the repository
```bash
git clone https://github.com/edgaregonzalez/nodejs-helloworld-api.git
```

### Install dependencies 

```bash
npm install
```

### Run the tests
```bash
npm test
```

### Start the server
```bash
npm start
```

### Make a request
```bash
curl http://localhost:3000
```

# **CI/CD**
---
## Paso a Paso para Configurar Jenkins con ngrok:

1. **Instalación de ngrok:**
   - Descarga ngrok desde su [página oficial](https://ngrok.com/download).
   - Sigue las instrucciones de instalación para tu sistema operativo.

2. **Exponer Jenkins usando ngrok:**
   - Abre una terminal y ejecuta el siguiente comando:
     ```
     ngrok http http://localhost:8080
     ```
   - Esto proporcionará un enlace público para acceder a Jenkins.
     - [Más información](https://postimg.cc/wyxCYR2s) : [![5.png](https://i.postimg.cc/wyxCYR2s)](https://postimg.cc/wyxCYR2s)

3. **Acceder a Jenkins a través de ngrok:**
   - Abre tu navegador web y ve al enlace proporcionado por ngrok.
     - Dirección IP [https://f9b1-2802-8010-821d-e200-b0b3-141-3b8b-4a06.ngrok-free.app](https://f9b1-2802-8010-821d-e200-b0b3-141-3b8b-4a06.ngrok-free.app)
     - Acceder a Jenkins (https://postimg.cc/K3zv2z7z) 

4. **Configuración del webhook en GitHub:**
   - En la configuración de tu repositorio en GitHub, agrega una nueva URL de webhook apuntando al enlace de ngrok para los eventos "push" y "pull request".
   - Configurar webhook en GitHub (https://postimg.cc/WdNs30F4) 
   - Seleccionar eventos en GitHub (https://postimg.cc/V5d8sN3P) 

5. **Configuración de Jenkins para recibir notificaciones de GitHub:**
   - En Jenkins, configura un nuevo pipeline o proyecto y agrega las credenciales de GitHub.
     - Asegúrate de agregar la URL del repositorio de GitHub.
     - (https://postimg.cc/CBbbb02h) 
   - Activar la opción "GitHub hook trigger for GITScm polling" en Jenkins para que se accione como un gatillo que activa la construcción automática del proyecto cuando se produce un cambio en el repositorio de GitHub
     -(https://postimg.cc/rKxHD9DL)

6. **¡Preparado para recibir commits!**
   - En este punto, Jenkins responderá automáticamente a los commits en tu repositorio.
   - (https://postimg.cc/47X9JWkx) 

### Verificación del Funcionamiento:

- Para verificar su funcionamiento y completar la documentación de este README, se realizaron múltiples cambios en la rama principal, que fueron recibidos exitosamente por el proceso de Entrega Continua (CD).
  - Proceso finalizado de buil: (https://postimg.cc/239N735H) 
  - Logs que muestra que se lanzao la tarea (https://postimg.cc/rRL31YsL) 

## Diagrama de alto nivel de la preparación del CI/CD
---

graph TD;
    A[Instalar ngrok] --> B[Ejecutar ngrok];
    B --> C[Acceder a Jenkins];
    C --> D[Configuracion del webhook en GitHub];
    D --> E[Configucion de Jenkins];
    E --> F[Puede recibir Commits];



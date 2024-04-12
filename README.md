# NodeJs, helloworld API for test propouses.

This is a simple API that returns a welcome message.

## Run your local environment

### Clone the repository
```bash
git clone https://github.com/edgaregonzalez/nodejs-helloworld-api.git
```

###### Install dependencies 
## pruebita commitada
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

# <span style="font-size:larger;">**CI/CD**</span>
---
## Paso a Paso para Configurar Jenkins con ngrok:

1. **Instalación de ngrok:**
   - Descarga ngrok desde su <a href="https://ngrok.com/download" style="color:green;">página oficial</a>.
   - Sigue las instrucciones de instalación para tu sistema operativo.

2. **Exponer Jenkins usando ngrok:**
   - Abre una terminal y ejecuta el siguiente comando:
     ```
     ngrok http http://localhost:8080
     ```
   - Esto proporcionará un enlace público para acceder a Jenkins.

3. **Acceder a Jenkins a través de ngrok:**
   - Abre tu navegador web y ve al enlace proporcionado por ngrok.
    - Dirección IP: <a href="https://f9b1-2802-8010-821d-e200-b0b3-141-3b8b-4a06.ngrok-free.app" style="color:red;">https://f9b1-2802-8010-821d-e200-b0b3-141-3b8b-4a06.ngrok-free.app</a>
    - <a href="https://postimg.cc/ZCjXRpFV" style="color:green;">Acceder a Jenkins</a> : <a href="https://postimg.cc/ZCjXRpFV"><img src="https://i.postimg.cc/kgdCTyV3/endopindt.png" alt="endopindt.png" style="border:1px solid green;"></a>

4. **Configuración del webhook en GitHub:**
   - En la configuración de tu repositorio en GitHub, agrega una nueva URL de webhook apuntando al enlace de ngrok para los eventos "push" y "pull request".
   - <a href="https://postimg.cc/WdNs30F4" style="color:green;">Configurar webhook en GitHub</a> : <a href="https://postimg.cc/WdNs30F4"><img src="https://i.postimg.cc/8zWcZHTL/asf.png" alt="asf.png" style="border:1px solid green;"></a>
   - <a href="https://postimg.cc/V5xMfWtc" style="color:green;">Seleccionar eventos en GitHub</a> : <a href="https://postimg.cc/V5xMfWtc"><img src="https://i.postimg.cc/653hhH5T/pyll.png" alt="pyll.png" style="border:1px solid green;"></a>

5. **Configuración de Jenkins para recibir notificaciones de GitHub:**
   - En Jenkins, configura un nuevo pipeline o proyecto y agrega las credenciales de GitHub.

   - Asegúrate de agregar la URL del repositorio de GitHub.

   - <a href="https://postimg.cc/yJRxrwfg" style="color:green;"><img src="https://i.postimg.cc/1zCF4SwH/qwr.png" alt="qwr.png" style="border:1px solid green;"></a>

   - Activar la opción "GitHub hook trigger for GITScm polling" en Jenkins para que se accione como un gatillo que activa la construcción automática del proyecto cuando se produce un cambio en el repositorio de GitHub

    - <a href="https://postimg.cc/rKxHD9DL" style="color:green;">Más información</a> : <a href="https://postimg.cc/rKxHD9DL"><img src="https://i.postimg.cc/Hsh1PZHj/4.png" alt="4.png" style="border:1px solid green;"></a>


6. **¡Preparado para recibir commits!**

   - En este punto, Jenkins responderá automáticamente a los commits en tu repositorio.

   - <a href="https://postimg.cc/47X9JWkx" style="color:green;"><img src="https://i.postimg.cc/tTxtNcBW/tyit.png" alt="tyit.png" style="border:1px solid green;"></a>


### Verificación del Funcionamiento:

- Para verificar su funcionamiento y completar la documentación de este README, se realizaron múltiples cambios en la rama principal, que fueron recibidos exitosamente por el proceso de Entrega Continua (CD).

- <a href="https://postimg.cc/239N735H" style="color:green;"><img src="https://i.postimg.cc/MKqZxQJ8/1.png" alt="1.png" style="border:1px solid green;"></a>
     
- <a href="https://postimg.cc/MvrRw0py" style="color:red;"><img src="https://i.postimg.cc/g2GKvN9B/2.png" alt="2.png" style="border:1px solid red;"></a>


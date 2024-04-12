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

# <span style="font-family:Arial, sans-serif; font-size:20px;">**CI/CD**</span>
---
## <span style="font-family:Arial, sans-serif; font-size:16px;">Paso a Paso para Configurar Jenkins con ngrok:</span>

1. **<span style="font-family:Arial, sans-serif; font-size:14px;">Instalación de ngrok:</span>**
   - <span style="font-family:Arial, sans-serif; font-size:14px;">Descarga ngrok desde su <a href="https://ngrok.com/download" style="color:green; text-decoration:none;">página oficial</a>.</span>
   - <span style="font-family:Arial, sans-serif; font-size:14px;">Sigue las instrucciones de instalación para tu sistema operativo.</span>

2. **<span style="font-family:Arial, sans-serif; font-size:14px;">Exponer Jenkins usando ngrok:</span>**
   - <span style="font-family:Arial, sans-serif; font-size:14px;">Abre una terminal y ejecuta el siguiente comando:</span>
     ```
     ngrok http http://localhost:8080
     ```
   - <span style="font-family:Arial, sans-serif; font-size:14px;">Esto proporcionará un enlace público para acceder a Jenkins.</span>
     - <span style="font-family:Arial, sans-serif; font-size:14px;"><a href="https://postimg.cc/wyxCYR2s" style="color:green; text-decoration:none;">Más información</a> : <a href="https://postimg.cc/wyxCYR2s">![5.png](https://i.postimg.cc/wyxCYR2s)</a></span>

3. **<span style="font-family:Arial, sans-serif; font-size:14px;">Acceder a Jenkins a través de ngrok:</span>**
   - <span style="font-family:Arial, sans-serif; font-size:14px;">Abre tu navegador web y ve al enlace proporcionado por ngrok.</span>
     - <span style="font-family:Arial, sans-serif; font-size:14px;">Dirección IP: <a href="https://f9b1-2802-8010-821d-e200-b0b3-141-3b8b-4a06.ngrok-free.app" style="color:red; text-decoration:none;">https://f9b1-2802-8010-821d-e200-b0b3-141-3b8b-4a06.ngrok-free.app</a></span>
     - <span style="font-family:Arial, sans-serif; font-size:14px;"><a href="https://postimg.cc/K3zv2z7z" style="color:green; text-decoration:none;">Acceder a Jenkins</a> : <a href="https://postimg.cc/K3zv2z7z"><img src="https://i.postimg.cc/endopindt/endopindt.png" alt="endopindt.png" style="border:1px solid green;"></a></span>

4. **<span style="font-family:Arial, sans-serif; font-size:14px;">Configuración del webhook en GitHub:</span>**
   - <span style="font-family:Arial, sans-serif; font-size:14px;">En la configuración de tu repositorio en GitHub, agrega una nueva URL de webhook apuntando al enlace de ngrok para los eventos "push" y "pull request".</span>
     - <span style="font-family:Arial, sans-serif; font-size:14px;"><a href="https://postimg.cc/WdNs30F4" style="color:green; text-decoration:none;">Configurar webhook en GitHub</a> : <a href="https://postimg.cc/WdNs30F4"><img src="https://i.postimg.cc/asf.png" alt="asf.png" style="border:1px solid green;"></a></span>
   - <span style="font-family:Arial, sans-serif; font-size:14px;"><a href="https://postimg.cc/V5d8sN3P" style="color:green; text-decoration:none;">Seleccionar eventos en GitHub</a> : <a href="https://postimg.cc/V5d8sN3P"><img src="https://i.postimg.cc/pyll.png" alt="pyll.png" style="border:1px solid green;"></a></span>

5. **<span style="font-family:Arial, sans-serif; font-size:14px;">Configuración de Jenkins para recibir notificaciones de GitHub:</span>**
   - <span style="font-family:Arial, sans-serif; font-size:14px;">En Jenkins, configura un nuevo pipeline o proyecto y agrega las credenciales de GitHub.</span>
     - <span style="font-family:Arial, sans-serif; font-size:14px;">Asegúrate de agregar la URL del repositorio de GitHub.</span>
     - <span style="font-family:Arial, sans-serif; font-size:14px;"><a href="https://postimg.cc/CBbbb02h" style="color:green; text-decoration:none;"><img src="https://i.postimg.cc/3.png" alt="3.png" style="border:1px solid green;"></a></span>
   - <span style="font-family:Arial, sans-serif; font-size:14px;">Activar la opción "GitHub hook trigger for GITScm polling" en Jenkins para que se accione como un gatillo que activa la construcción automática del proyecto cuando se produce un cambio en el repositorio de GitHub</span>
     - <span style="font-family:Arial, sans-serif; font-size:14px;"><a href="https://postimg.cc/rKxHD9DL" style="color:green; text-decoration:none;">Más información</a> : <a href="https://postimg.cc/rKxHD9DL"><img src="https://i.postimg.cc/4.png" alt="4.png" style="border:1px solid green;"></a></span>

6. **<span style="font-family:Arial, sans-serif; font-size:14px;">¡Preparado para recibir commits!</span>**
   - <span style="font-family:Arial, sans-serif; font-size:14px;">En este punto, Jenkins responderá automáticamente a los commits en tu repositorio.</span>
     - <span style="font-family:Arial, sans-serif; font-size:14px;"><a href="https://postimg.cc/47X9JWkx" style="color:green; text-decoration:none;"><img src="https://i.postimg.cc/tyit.png" alt="tyit.png" style="border:1px solid green;"></a></span>

### <span style="font-family:Arial, sans-serif; font-size:16px;">Verificación del Funcionamiento:</span>

- <span style="font-family:Arial, sans-serif; font-size:14px;">Para verificar su funcionamiento y completar la documentación de este README, se realizaron múltiples cambios en la rama principal, que fueron recibidos exitosamente por el proceso de Entrega Continua (CD).</span>

  - <span style="font-family:Arial, sans-serif; font-size:14px;"><a href="https://postimg.cc/239N735H" style="color:green; text-decoration:none;"><img src="https://i.postimg.cc/1.png" alt="1.png" style="border:1px solid green;"></a></span>
  
  - <span style="font-family:Arial, sans-serif; font-size:14px;"><a href="https://postimg.cc/rRL31YsL" style="color:green; text-decoration:none;"><img src="https://i.postimg.cc/2.png" alt="2.png" style="border:1px solid green;"></a></span>


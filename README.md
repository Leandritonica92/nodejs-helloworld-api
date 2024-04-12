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
### CI/CD

# <span style="font-size:larger;">**CI/CD**</span>
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

3. **Acceder a Jenkins a través de ngrok:**
   - Abre tu navegador web y ve al enlace proporcionado por ngrok.
     - Dirección IP: [https://f9b1-2802-8010-821d-e200-b0b3-141-3b8b-4a06.ngrok-free.app](https://f9b1-2802-8010-821d-e200-b0b3-141-3b8b-4a06.ngrok-free.app)
     - [Acceder a Jenkins](https://postimg.cc/ZCjXRpFV) : [![endopindt.png](https://i.postimg.cc/kgdCTyV3/endopindt.png)](https://postimg.cc/ZCjXRpFV)

4. **Configuración del webhook en GitHub:**
   - En la configuración de tu repositorio en GitHub, agrega una nueva URL de webhook apuntando al enlace de ngrok.
   - Selecciona los eventos deseados que desencadenarán el webhook.

5. **Configuración de Jenkins para recibir notificaciones de GitHub:**
   - En Jenkins, configura un nuevo pipeline o proyecto y agrega las credenciales de GitHub.

6. **¡Preparado para recibir commits!**
   - A partir de este punto, Jenkins responderá automáticamente a los commits en tu repositorio.

### Verificación del Funcionamiento:

Para verificar su funcionamiento y completar la documentación de este README, se realizaron múltiples cambios en la rama principal, que fueron recibidos exitosamente por el proceso de Entrega Continua (CD).

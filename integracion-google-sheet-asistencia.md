# Formulario de asistencia

La web conserva la URL de Apps Script configurada anteriormente en `app.js`, en la constante `assistanceEndpoint`:

https://script.google.com/macros/s/AKfycbxlG32r0qH5MEjenSVBpeqAbJ2bkimRaU7_mJdddmXSvlKgpvAbtB0PZs8TIJLMbuM/exec

El formulario envia por POST estos campos:

`fecha`, `nombre`, `cargo`, `municipalidad`, `region`, `provincia`, `distrito`, `correo`, `telefono`, `fase`, `necesidad`.

La hoja usada anteriormente para las solicitudes es:

https://docs.google.com/spreadsheets/d/1oTEStAnbTAOVkOCb5ZhWTUqWG4bKXxrlpL2zAmk06UY/edit?usp=sharing

El destino efectivo de cada envio depende del codigo y la implementacion del Apps Script. La direccion de la hoja no esta incluida en el envio del navegador.

## Estructura de seguimiento

La pestana `Solicitudes` utiliza estas 16 columnas:

`fecha`, `nombre`, `cargo`, `municipalidad`, `region`, `provincia`, `distrito`, `correo`, `telefono`, `fase`, `necesidad`, `estado`, `prioridad`, `responsable`, `ultima_atencion`, `proxima_accion`.

Los ultimos cinco campos se gestionan en la hoja o se inicializan en el servidor. No se solicitan al funcionario en la web.

## Comprobar la conexion despues de publicar

1. Abre la web publicada y entra al formulario de asistencia.
2. Envia una solicitud de prueba identificada como `PRUEBA`.
3. Abre tu hoja y comprueba que aparezca una nueva fila con region, provincia y distrito separados.
4. Si no aparece, revisa las ejecuciones y la implementacion del Apps Script. Confirma que el script use la hoja y la pestana correctas.

La web usa `no-cors`: el navegador no puede leer la respuesta de Apps Script para confirmar que la fila se guardo. La comprobacion en la hoja es necesaria para verificar la recepcion.

Esta entrega recupera los archivos de la web y actualiza los enlaces a documentos. No modifica la implementacion de Apps Script ni los permisos de la hoja.

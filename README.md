# Backend-DevOps

Funcionalidades de Nodepop

- Listar tags de anuncios: GET : 
      
    http://ec2-23-22-11-75.compute-1.amazonaws.com/api/v1/anuncios/tags

- Listar anuncios: GET:

  * Todos los anuncios, admite cualquier cadena como token
  
    http://ec2-23-22-11-75.compute-1.amazonaws.com/api/v1/anuncios?token=whdihwihd

  * Filtrar anuncios. Admite los siguientes filtros: nombre: admite las primeras letras del nombre y es no case sensitive venta: true | false precio: rangos 10-50, 10-, -50, 50 tag start limit sort includeTotal: true | false añade una fila con el total de anuncios listados. Además debe incluir un token.
  
    http://ec2-23-22-11-75.compute-1.amazonaws.com/api/v1/anuncios?tag=mobile&venta=false&nombre=ip&precio=50&start=0&limit=2&sort=precio&includeTotal=true&token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJfaWQiOiI1NWZk 

  * Registrar usuarios nuevos, con Postman: POST : 
    
    http://ec2-23-22-11-75.compute-1.amazonaws.com/api/v1/usuarios/register

    body : x-www.form-urlencoded 
      nombre : 
      email : 
      clave :


  * Autenticar un usuario: POST : 
  
    http://ec2-23-22-11-75.compute-1.amazonaws.com/api/v1/usuarios/authenticate

    body : x-www.form-urlencoded 
      email : 
      clave :


  *  Guardar token: PUT : 
  
    http://ec2-23-22-11-75.compute-1.amazonaws.com/api/v1/usuarios/pushtoken

    body : x-www.form-urlencoded 
      plataforma : [‘ios’, android’] 
      token: 
      usuario :


  * Visualización de imágenes. Los archivos estáticos, como las imágenes, se sirven por nginx y no por nodepop. La cabecera personalizada es X-Author: @verocordobes 
   
    http://ec2-23-22-11-75.compute-1.amazonaws.com/images/anuncios/iphone.png 
    http://ec2-23-22-11-75.compute-1.amazonaws.com/images/anuncios/bicicleta.png


Indicando la IP del servidor se muestra el contenido de la plantilla personalizada:

http://23.22.11.75/

Y también en el dominio creado para la clase :)

veronicacordobes.es

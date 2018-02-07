# Prueba de conocimiento

Esta prueba consiste en implementar un pequeño módulo de autenticación y gestión de usuarios con el framework Yii 2.0 y con MySQL

Las métricas para el desarrollo de esta prueba son:

1. Crear la base de datos con el fichero sql/prueba_cv.sql
2. Crear el modelo User y adicionar sus respectivas implementaciones
3. Creación de usuarios
    * Crear el formulario con sus respectivos campos (el avatar es un widget)
    * Al crear el usuario el tipo de documento y el número de documento se almacenan por separado
    * El número de documento (Incluyendo el prefijo de tipo de documento) y el email son únicos (Validarlos en las reglas del modelo)
    * Crear Widget de subir avatar que permita realizar la previsualización de la foto antes de enviar el formulario
    * Adicionar funcionalidad en el controlador que permita subir un avatar
    * Encriptar la contraseña con md5

4. Listado de usuarios
    * En el grid view donde se visualiza los usuarios registrados visualizar una única columna para el numero de identificación de esta forma CC 1245324578 CE 4212364869 y realizar el ajuste respectivo en el input search de la columna
    * Visualizar la imagen del avatar en una columna en un tamaño de 40px por 40px;

5. Actualización de usuarios
    * Ajustar la esta funcionalidad para el cambio de password
    * Ajustar la esta funcionalidad para el cambio del avatar

6. Eliminación de usuarios
    * Ajustar la esta funcionalidad para la eliminación del avatar del disco duro

7. Autenticación
    * Autenticar con el número de identificación anteponiendo el prefijo de tipo de documento ejemplo CC1245324578 CE4212364869
    * Visualizar el avatar del usuario en las áreas correspondientes del admin template

### Tips y sugerencias
  - Para llevar a cabo esta prueba de manera exitosa utilizar el Generador de CRUD Y de Modelos (GII) 
  - Revisar la documentación del active record de Yii2
  - Utilizar al máximo los **Core Helper Classes** proporciona Yii 2.0 **!!Es opcional, sumaran puntos apreciativos para la prueba**
  - Para realizar el widget usar la clase **yii\web\UploadedFile** y para previsualizar la foto usar jQuery (evento on change)
  - Para que la implementación del login sea más fácil, en el proyecto ya se encuentra un modelo de prueba, se sugiere renombrarlo y con el nuevo modelo del active record adicionar las implementaciones de **IdentityInterface**
  - También hay un modelform que se conecta a la vista del login, este es el encargado de la lógica de la autenticación
  - Se sugiere Utilizar MySQL Workbench para administrar la base de datos, o de otro modo phpmyadmin
  - Recuerde que este framework emplea composer como administrador de librerías de terceros
  - Para arrancar el proyecto se puede hacer dos formas: Por la consola con el comando **yii serve** o creando un alias hacia **prueba_cv/web**

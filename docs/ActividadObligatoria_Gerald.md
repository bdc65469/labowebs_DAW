---
author: Gerald
title: Práctica de Git

---

# Ejercicio de git - Proyecto labowebs 

> Gerald Alexis Rueda Tejedo

[TOC]







<u>**URL al repositorio Github: https://github.com/bdc65469/labowebs_DAW.git**</u>

<div style="page-break-after: always; break-after: page;"></div>



## Trabajo en local

### Cuestiones

1. **Inicializa un nuevo repositorio Git en una carpeta llamada `"labowebs"` y agrega los archivos proporcionados en el aula virtual. Renombra la rama master a `main`, si es necesario. Realiza el primer commit. Muestra el log del repositorio.**

   ```bash
   git init
   git add .
   git commit -m "Primer commit"
   git log
   ```

   ![image-20241114090450176](./ActividadObligatoria_Gerald.assets/image-20241114090450176.png)

   ![image-20241114090524583](./ActividadObligatoria_Gerald.assets/image-20241114090524583.png)

   

2. **Incluye un fichero `.gitignore` para que los ficheros `README.md` , `LICENCE.txt` y `passwords.txt` sean ignorados por el control de versiones. Realiza el commit y muestra los logs del repositorio en una línea.**

   ```bash
   gedit .gitignore
   git add .gitigore
   git commit -m ".gitignore añadido"
   git log --oneline
   ```

   ![image-20241114091831778](./ActividadObligatoria_Gerald.assets/image-20241114091831778.png)

   ![image-20241114091026420](./ActividadObligatoria_Gerald.assets/image-20241114091026420.png)

   

3. **En el repositorio, crea los archivos `README.md` , `LICENCE.txt` y `passwords.txt` con algún contenido. Muestra el estado del repositorio. Muestra el listado de archivos ignorados.**

     ```bash
     echo "Este es el archivo readme" > README.md
     echo "Este es el archivo de licencias" > LICENCE.txt
     echo "Este es el archivo de password" > password.txt
     git status
     git ls-files --others --ignored --exclude-standard
     ```

     ![image-20241114092250332](./ActividadObligatoria_Gerald.assets/image-20241114092250332.png)

     ![image-20241114092320473](./ActividadObligatoria_Gerald.assets/image-20241114092320473.png)

     ![image-20241114092418331](./ActividadObligatoria_Gerald.assets/image-20241114092418331.png)

     

4. **Crea una rama `feature-estilos` . Cámbiate a ella.** 

     ```bash
     git checkout -b feature-estilos
     ```

     ![image-20241114092710505](./ActividadObligatoria_Gerald.assets/image-20241114092710505.png)

     - Modifica el archivo estilos.css :

       -   propiedad color del `body` y de `h2` : #2a2a2a

       -   propiedad `background-color` de `header` y `footer`: `#2a75ff`

         ![image-20241114093004078](./ActividadObligatoria_Gerald.assets/image-20241114093004078.png)

       -   Comprueba el estado del repositorio. Añade los cambios, realiza un commit con el mensaje "actualizados estilos a azules"

         ```bash
         git status
         git add css/estilos.css
         git commit -m "actualizados estilos a azules"
         ```

         ![image-20241114093140266](./ActividadObligatoria_Gerald.assets/image-20241114093140266.png)
         
         

5. **Vuelve a la rama `main` . En el archivo `index.htm`l añade un comentario donde se indique tu nombre como autor de la página. Comprueba el estado del repositorio. Añade los cambios, realiza un commit con el mensaje ' añadido autor en index'. Muestra los logs del repositorio en una línea, gráficamente y con 'decoración'**

     ```bash
     git checkout main
     git status
     git add index.html
     git commit -m "añadido autor en index"
     git log --oneline --graph --all -decorate
     ```

     ![image-20241114093341108](./ActividadObligatoria_Gerald.assets/image-20241114093341108.png)

     ![image-20241114093436960](./ActividadObligatoria_Gerald.assets/image-20241114093436960.png)

     ![image-20241114093635653](./ActividadObligatoria_Gerald.assets/image-20241114093635653.png)

     ![image-20241114093659890](./ActividadObligatoria_Gerald.assets/image-20241114093659890.png)

     

6. **Fusiona la rama `feature-estilos` en la rama `main` . Muestra los logs del repositorio en una línea, gráficamente y con 'decoración'**

     ```bash
     git merge feature-estilos
     git log --oneline --graph --all -decorate
     
     ```

     ![image-20241114093919466](./ActividadObligatoria_Gerald.assets/image-20241114093919466.png)

![image-20241114093852973](./ActividadObligatoria_Gerald.assets/image-20241114093852973.png)

![image-20241114093948231](./ActividadObligatoria_Gerald.assets/image-20241114093948231.png)

<div style="page-break-after: always; break-after: page;"></div>





## Trabajo en remoto

### Cuestiones

1. **Continúa con el repositorio `labowebs` . Añade el repositorio a Sourcetree**

   ![image-20241114095400706](./ActividadObligatoria_Gerald.assets/image-20241114095400706.png)

2. **Crea un repositorio remoto y sube al remoto los ficheros de tu repositorio local. Debes subir todas las ramas.**

  ![image-20241114100115607](./ActividadObligatoria_Gerald.assets/image-20241114100115607.png)

  Configurar el repositorio remoto

  ![image-20241114100421593](./ActividadObligatoria_Gerald.assets/image-20241114100421593.png)

  ![image-20241114100309639](./ActividadObligatoria_Gerald.assets/image-20241114100309639.png)

  Para subirlo clicamos en el boton `push`

  ![image-20241114100912415](./ActividadObligatoria_Gerald.assets/image-20241114100912415.png)

  

  Añadimos las dos ramas

  ![image-20241114100722046](./ActividadObligatoria_Gerald.assets/image-20241114100722046.png)

  Ya esta subido



  ![image-20241114100817257](./ActividadObligatoria_Gerald.assets/image-20241114100817257.png)



3. **Crea una rama `feature-index` . Añade el siguiente código dentro de la `<section class="about">` . Añade los cambios y crea un commit. Sube los cambios al remoto.**

  Para crear una nueva rama, clicamos en el boton `branch` y escribimos el nombre de la rama

  ![image-20241114101120924](./ActividadObligatoria_Gerald.assets/image-20241114101120924.png)

  <img src="./ActividadObligatoria_Gerald.assets/image-20241114101330386.png" alt="image-20241114101330386" style="zoom: 80%;" />

  Para añadir los cambios

  ![image-20241114101518209](./ActividadObligatoria_Gerald.assets/image-20241114101518209.png)

  Para hacer el commit

  ![image-20241114101602727](./ActividadObligatoria_Gerald.assets/image-20241114101602727.png)

  Vemos los cambios

  ![image-20241114101649119](./ActividadObligatoria_Gerald.assets/image-20241114101649119.png)

  Para subirlos al remoto, clicamos en el boton `push` y elegimos la rama/s que queremos subir

  ![image-20241114101804002](./ActividadObligatoria_Gerald.assets/image-20241114101804002.png)

  

4. **En el repositorio local, fusiona la rama `feature-index` en la rama `main` .**

   Nos movemos a la rama donde queremos aplicar los cambios, para ello damos click derecho sobrea la rama y pulsamos en ceckout <nombre de la rama>

   ![image-20241114133220082](./ActividadObligatoria_Gerald.assets/image-20241114133220082.png)

   Ahora debemos hacer click derecho sobre la rama que queremos fusionar y le damos a la opción de merge

   ![image-20241114133345247](./ActividadObligatoria_Gerald.assets/image-20241114133345247.png)

   ![image-20241114133450987](./ActividadObligatoria_Gerald.assets/image-20241114133450987.png)

   

   

5. **Edita el fichero contacto.html . Borra unas líneas. Muestra los ficheros con cambios pendientes y las diferencias. Añade los cambios y haz un commit.**

   Vamos a borrar lo siguiente

   ![image-20241114135258062](./ActividadObligatoria_Gerald.assets/image-20241114135258062.png)

   ![image-20241114135405645](./ActividadObligatoria_Gerald.assets/image-20241114135405645.png)

   Vamos añadir los cambios y a hacer un commit

   ![image-20241114135457029](./ActividadObligatoria_Gerald.assets/image-20241114135457029.png)

   ![image-20241114135526797](./ActividadObligatoria_Gerald.assets/image-20241114135526797.png)

   

6. **Te das cuenta del error. Deshaz el commit anterior. Captura el estado actual del repositorio.**

   Para revertir un commit damos click derecho sobre el commit y le damos a la opción de reverse commit

   ![image-20241114135640340](./ActividadObligatoria_Gerald.assets/image-20241114135640340.png)

   ![image-20241114135728134](./ActividadObligatoria_Gerald.assets/image-20241114135728134.png)

   ![image-20241114135823733](./ActividadObligatoria_Gerald.assets/image-20241114135823733.png)

   

7. **Crea una rama `feature-mapa` . Incluye este código en el archivo `contacto.html` . Añade los cambios. Realiza un commit. Sube los cambios al remoto. Muestra en el remoto los cambios del archivo `contacto.html` en la rama `feature-mapa` .**

Creamos la rama `feature-mapa`

![image-20241114135931743](./ActividadObligatoria_Gerald.assets/image-20241114135931743.png)

Añadimos los cambios y hacemos el commit

![image-20241114140110537](./ActividadObligatoria_Gerald.assets/image-20241114140110537.png)

![image-20241114140203135](./ActividadObligatoria_Gerald.assets/image-20241114140203135.png)

Ahora vamos a subirlo a nuestro repositorio remoto

![image-20241114140529872](./ActividadObligatoria_Gerald.assets/image-20241114140529872.png)

![image-20241114140612696](./ActividadObligatoria_Gerald.assets/image-20241114140612696.png)

Vemos como ya se han subido los cambios a nuestro repositorio remoto 

![image-20241114140815114](./ActividadObligatoria_Gerald.assets/image-20241114140815114.png)



8.**En GitHub, en la rama `main` , fusiona la rama `feature-mapa` . Baja los cambios del remoto a local. Deja los dos repositorios sincronizados.**

![image-20241114141010905](./ActividadObligatoria_Gerald.assets/image-20241114141010905.png)

Le damos a `merge pull request`

![image-20241114141147885](./ActividadObligatoria_Gerald.assets/image-20241114141147885.png)

Confirmamos el merge

![image-20241114141207645](./ActividadObligatoria_Gerald.assets/image-20241114141207645.png)

Vemos que en la rama `main`, ya están aplicados también los cambios en contacto

![image-20241114141338819](./ActividadObligatoria_Gerald.assets/image-20241114141338819.png)

Por último vamos a hacer el `pull` para que nuestro repositorio remoto y local tengan el mismo contenido

<div style="page-break-after: always; break-after: page;"></div>



## Conflictos 

### Cuestiones

1. **Crea una rama `hotfix-js` . Cámbiate a ella. Añade este código en el fichero `script.js` .Confirma el cambio y haz un commit. (Fíjate en los números de línea...)**

  Creamos la rama

  ![image-20241115084238365](./ActividadObligatoria_Gerald.assets/image-20241115084238365.png)

  Añadimos el código nuevo

  ![image-20241115084413626](./ActividadObligatoria_Gerald.assets/image-20241115084413626.png)

  Añadimos los cambios

  ![image-20241115084502833](./ActividadObligatoria_Gerald.assets/image-20241115084502833.png)

  Y hacemos el commit

  ![image-20241115084541928](./ActividadObligatoria_Gerald.assets/image-20241115084541928.png)

  

2. **Vuelve a la rama main . En el fichero script.js en las mismas líneas que en la cuestión anterior, añade el código siguiente. Confirma el cambio y haz un commit.**

  Nos cambiamos a la rama main, para ello click derecho sobre el nombre de la rama y `checkout main`

  ![image-20241115084641460](./ActividadObligatoria_Gerald.assets/image-20241115084641460.png)

  Modificamos el fichero `script.js`

  ![image-20241115084811621](./ActividadObligatoria_Gerald.assets/image-20241115084811621.png)

  Añadimos los cambios

  ![image-20241115085047502](./ActividadObligatoria_Gerald.assets/image-20241115085047502.png)

  Hacemos el commit

  ![image-20241115085133571](./ActividadObligatoria_Gerald.assets/image-20241115085133571.png)

  

3. **Fusiona la rama `hotfix-js` en `main` . Debe producirse un conflicto. Resuélvelo. Cuando termines la resolución del conflicto sube los cambios al remoto - Deja los repositorios sincronizados -**

  Para fusionar la rama main con la rama `hotfix-js`, nos situamos en la rama main y damos click derecho sobre la rama `hotfix-js` y elegimos la opción `merge hotfix-js into current branch`

  ![image-20241115085313198](./ActividadObligatoria_Gerald.assets/image-20241115085313198.png)

  ![image-20241115085347319](./ActividadObligatoria_Gerald.assets/image-20241115085347319.png)

  Y nos muestra que hay un conflicto

  ![image-20241115085429188](./ActividadObligatoria_Gerald.assets/image-20241115085429188.png)

  Abrimos el visual studio code para resolver el conflicto

  ![image-20241115085746364](./ActividadObligatoria_Gerald.assets/image-20241115085746364.png)

  Tenemos para opciones para resolver el conflicto, en este caso vamos a aceptar cambio actual

  ![image-20241115085847405](./ActividadObligatoria_Gerald.assets/image-20241115085847405.png)

  Vemos que se mantiene el último cambio y se resolvió el conflicto

  Por último vamos a hacer el push de la rama main a nuestro repositorio remoto

  ![image-20241115090032227](./ActividadObligatoria_Gerald.assets/image-20241115090032227.png)

  Vemos como en github se ha subio nuestro fichero `script.js` con la última versión

  ![image-20241115090145371](./ActividadObligatoria_Gerald.assets/image-20241115090145371.png)

# Fractal Magick
Es un script sencillo y basico, que nacio como practica introductoria para escribir en Bash Script.
Usa la libreria Image Magick y los efectos usados son los pueblicados en el sitio [http://www.fmwconcepts.com/imagemagick/](http://www.fmwconcepts.com/imagemagick/)

## Modo de uso:
*fractalmagick 'URL' nombreArchivo*

Donde la URL tiene que ser una imagen en jpg y **debe estar entre comillas**. El segundo parametro es el nombre que recive el archivo cuando se descarga... 

Si uno usa el mismo nombre que un archivo existente, estos archivos se sobre escriben (bug)

Por lo tanto si tengo la foto, "fulano" conviene y se aconseja usar el nombre "fulano0" y para la siguiente "fulano1" y a si sucesivamente.

## Efectos Disponibles

 - [kaleidoscopic](http://www.fmwconcepts.com/imagemagick/kaleidoscopic/index.php)
 - [pixelize](http://www.fmwconcepts.com/imagemagick/pixelize/index.php)
 - [recursion](http://www.fmwconcepts.com/imagemagick/recursion/index.php)
 - [vintage2](http://www.fmwconcepts.com/imagemagick/vintage2/index.php)
 - [thermography](http://www.fmwconcepts.com/imagemagick/thermography/index.php)
 - [kmeans](http://www.fmwconcepts.com/imagemagick/kmeans/index.php)
 - [stutter](http://www.fmwconcepts.com/imagemagick/stutter/index.php)



## To Do
 - Opcion para imagen descargada o local 
 - Que pasa con imagenes que no son JPG?
 - Como aplicar los efectos? En que orden ?
 - Usar arrays para cargar configuraciones de los efectos, y mejorar el nombramiento de los archivos (automatisar todo un poco mas )
 - Hacer comprobaciones existe ristretto? kaleidoscopic? wget?
 - Mejorar instalador ?
 - Tomar deciciones con respecto a los nombres de archivos... para no pisar el mismo archivo, por un tema de coincidencia de nombre

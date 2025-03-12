<h1>Uso de ExifTool</h1>

<p><strong>ExifTool</strong> es una herramienta poderosa para <strong>leer, crear y modificar metadatos</strong> en una amplia variedad de archivos, incluidos los metadatos <strong>EXIF, IPTC, XMP</strong>, entre otros. Aquí te dejo cómo hacerlo paso a paso.</p>

<h2>1. Leer Metadatos con ExifTool</h2>

<p>Para <strong>leer los metadatos de un archivo</strong>, puedes usar el siguiente comando:</p>

<pre><code>exiftool nombre_del_archivo</code></pre>

<p><strong>Ejemplo:</strong></p>

<pre><code>exiftool imagen.jpg</code></pre>

<h2>2. Crear o Modificar Metadatos con ExifTool</h2>

<p>Puedes <strong>agregar o modificar</strong> los metadatos de un archivo utilizando ExifTool. A continuación, algunos ejemplos de cómo hacerlo:</p>

<h3>a. Modificar la fecha y hora de una imagen</h3>
<p>Para <strong>cambiar la fecha y hora de la imagen</strong> (en el formato <code>yyyy:mm:dd hh:mm:ss</code>):</p>

<pre><code>exiftool -DateTimeOriginal="2025:01:19 15:30:00" nombre_del_archivo.jpg</code></pre>

<h3>b. Agregar o modificar la geolocalización (latitud y longitud)</h3>
<p>Si deseas <strong>agregar una ubicación</strong> (por ejemplo, latitud 40.7128 y longitud -74.0060), usa el siguiente comando:</p>

<pre><code>exiftool -GPSLatitude=40.7128 -GPSLongitude=-74.0060 nombre_del_archivo.jpg</code></pre>

<h3>c. Modificar el autor o el título</h3>
<p>Si deseas <strong>agregar o cambiar el autor</strong> de la imagen o el <strong>título</strong>, puedes usar:</p>

<pre><code>exiftool -Artist="Juan Pérez" -Title="Viaje a la ciudad" nombre_del_archivo.jpg</code></pre>

<h3>d. Eliminar un metadato específico</h3>
<p>Si deseas <strong>eliminar un metadato específico</strong>, como la ubicación GPS, usa:</p>

<pre><code>exiftool -GPSLatitude= -GPSLongitude= nombre_del_archivo.jpg</code></pre>

<p>Esto eliminará la <strong>información de geolocalización</strong> de la imagen.</p>

<h2>3. Crear Metadatos en un Archivo</h2>

<p>Si deseas <strong>agregar metadatos desde cero</strong>, puedes hacerlo especificando los campos que quieres agregar. Ejemplo para <strong>agregar un comentario</strong>:</p>

<pre><code>exiftool -Comment="Este es un comentario personalizado" nombre_del_archivo.jpg</code></pre>

<h2>4. Guardar los cambios en un nuevo archivo</h2>

<p>Por defecto, ExifTool crea una <strong>copia de respaldo</strong> del archivo original con la extensión <code>_original</code>. Si no quieres que ExifTool cree un archivo de respaldo, puedes usar la opción <code>-overwrite_original</code>:</p>

<pre><code>exiftool -overwrite_original -Title="Nueva Titulo" nombre_del_archivo.jpg</code></pre>

<h2>5. Ver todos los metadatos posibles</h2>

<p>Para <strong>ver todos los metadatos disponibles</strong> en un archivo (incluyendo EXIF, IPTC, XMP), puedes utilizar:</p>

<pre><code>exiftool -a -u -g nombre_del_archivo.jpg</code></pre>

<p>Esto mostrará <strong>todos los metadatos agrupados</strong> y te dará una vista más detallada de los datos disponibles.</p>

<h2>Consejos adicionales</h2>

<p><strong>ExifTool</strong> también permite procesar <strong>múltiples archivos a la vez</strong>. Por ejemplo, para cambiar los metadatos de todas las imágenes en una carpeta:</p>

<pre><code>exiftool -Artist="Juan Pérez" *.jpg</code></pre>

<p>Si deseas realizar <strong>cambios masivos a muchos archivos</strong>, puedes usar filtros, como modificar solo las imágenes con una <strong>fecha de creación específica</strong>.</p>

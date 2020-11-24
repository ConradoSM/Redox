<h1>Redox</h1>
<p>v 1.0.0</p>
<h2>Guía de instalación del entorno de desarrollo</h2>
<p>1. Hacer un fork del proyecto desde GitHub y lo clonarlo a nuestro directorio local</p>
<p><code>git clone git@github.com:<b>[USER]</b>/Redox.git</code></p>
<p>2. Levantar los contenedores</p>
<p><code>docker-compose up --build</code></p>
<p>3. Instalar las dependencias</p>
<p><code>docker-compose exec app composer install</code></p>
<p>4. Generar el archivo <b>.env</b></p>
<p><code>cp .env.example .env</code></p>
<p>5. Crear las migraciones</p>
<p><code>docker-compose exec app php artisan migrate</code></p>
<p>6. Generar key y configurar cache</p>
<p><code>docker-compose exec app php artisan key:generate</code></p>
<p><code>docker-compose exec app php artisan config:cache</code></p>
<p><code>docker-compose exec app php artisan config:clear</code></p>
<p>7. Instalar paquetes con <b>NPM</b></p>
<p><code>docker-compose exec app npm install</code></p>
<p>8. Compilar paquetes</p>
<p><code>docker-compose exec app npm run dev</code></p>
<p>9. Generar el acceso directo a la carpeta storage</p>
<p><code>docker-compose exec app php artisan storage:link</code></p>
<p>10. Editar el archivo <b>etc/hosts</b></p>
<p><code>127.0.0.1 local.redox.io</code></p>
<p>11. Probar el sitio</p>
<p><code>http://local.redox.io/</code></p>

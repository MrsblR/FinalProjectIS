# Proyecto Final de Ingeniería de Software II: Scooby Attendance

<p align="center">
  <img src="https://github.com/VILLA7523/theoriginscooby/blob/main/WEB/src/public/images/logodog.png?raw=true" alt="Sublime's custom image"/>
</p>

## Integrantes 
- Merisabel Ruelas Quenaya
- Fiorela Estefany Villarroel Ramos
- Juan Manuel Soto Begazo

## ¿Qué es Scooby Attendance?
El proceso de control de la asistencia en cualquier institución es una parte importante para determinar la eficacia de los servicios ofrecidos por la misma y el interés general de quienes se benefician de los servicios de la institución, en nuestro caso, los estudiantes. Este proceso es una rutina engorrosa, y por ello, el presente artículo propone una nueva forma de reemplazar el antiguo sistema, que implica registros de asistencia que tienen que ser llenados uno por uno para cada alumno, ya que este método requiere mucho tiempo y es propenso a cometer errores, ya sea marcando a un alumno como ausente por error o contando un número erróneo de asistencias cuando hay que entregar informes o estadísticas.

## Construción Automática
Para este proceso se utilizará el generador de aplicaciones, express, para crear rápidamente un esqueleto de aplicación.

Se instala de la siguiente forma:

```js
$ npm express-generator
```
Se muestran las opciones de mandato con la opción -h:
```js
$ express -h

  Usage: express [options][dir]

  Options:

    -h, --help          output usage information
        --version       output the version number
    -e, --ejs           add ejs engine support
        --hbs           add handlebars engine support
        --pug           add pug engine support
    -H, --hogan         add hogan.js engine support
        --no-view       generate without view engine
    -v, --view &lt;engine&gt; add view &lt;engine&gt; support (ejs|hbs|hjs|jade|pug|twig|vash) (defaults to jade)
    -c, --css &lt;engine&gt;  add stylesheet &lt;engine&gt; support (less|stylus|compass|sass) (defaults to plain css)
        --git           add .gitignore
    -f, --force         force on non-empty directory
 ```
 
 
Por ejemplo, nuestro código siguiente crea una aplicación Express denominada "myapp". La aplicación será creada en una carpeta llamada myapp en el directorio de trabajo actual y el motor de vistas será asignado a Pug:

```js
$ express --view=pug myapp

   create : myapp
   create : myapp/package.json
   create : myapp/app.js
   create : myapp/public
   create : myapp/public/javascripts
   create : myapp/public/images
   create : myapp/routes
   create : myapp/routes/index.js
   create : myapp/routes/users.js
   create : myapp/public/stylesheets
   create : myapp/public/stylesheets/style.css
   create : myapp/views
   create : myapp/views/index.pug
   create : myapp/views/layout.pug
   create : myapp/views/error.pug
   create : myapp/bin
   create : myapp/bin/www
 ```
A continuación, instale las dependencias:

```js
$ cd myapp
$ npm install
```

En Windows, utilizamos este mandato:

```js
> set DEBUG=myapp:* & npm start
```
A continuación, cargamos http://localhost:3000/ en el navegador para acceder a la aplicación.

La aplicación generada tiene la siguiente estructura de directorios:

```js
.
├── app.js
├── bin
│   └── www
├── package.json
├── public
│   ├── images
│   ├── javascripts
│   └── stylesheets
│       └── style.css
├── routes
│   ├── index.js
│   └── users.js
└── views
    ├── error.pug
    ├── index.pug
    └── layout.pug

7 directories, 9 files
```

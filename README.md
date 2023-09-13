# [Máster en Ingeniería Web por la Universidad Politécnica de Madrid (miw-upm)](http://miw.etsisi.upm.es)
# Back-end con Tecnologías de Código Abierto: **SPRING & PYTHON**
> Proyecto TPV. Este proyecto es un apoyo docente de la asignatura. Es una aplicación completa realizada con un Front-end con Angular, 
dos Back-ends con Spring y un Back-end con Python. El Back-end-user se desarrolla con programación síncrona y Postgresql. El Back-end-core s
 realiza con programación reactiva y MongoDB. El Back-end-customer-support con programación síncrona y MongoDB

## Tecnologías necesarias
`Java` `Maven` `Spring-Boot` `Reactor` `Python` `Angular` `MondoDB` `JPA` `SQL` `GitHub` `Travis-CI` `Sonarcloud` `Better Code Hub` `Heroku`

## Estado del código
Proyecto | GitHub - CI | Sonarcloud
-- | -- | --
Front-end-angular | [![Angular - Tests](https://github.com/miw-upm/betca-tpv-angular/actions/workflows/angular-test-sonar.yml/badge.svg)](https://github.com/miw-upm/betca-tpv-angular/actions/workflows/angular-test-sonar.yml) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=es.upm.miw%3Abetca-tpv-angular&metric=alert_status)](https://sonarcloud.io/dashboard?id=es.upm.miw%3Abetca-tpv-angular)
Back-end-user | [![Spring User - Tests](https://github.com/miw-upm/betca-tpv-user/workflows/Spring%20User%20-%20Tests/badge.svg)](https://github.com/miw-upm/betca-tpv-user/actions) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=es.upm.miw%3Abetca-tpv-user&metric=alert_status)](https://sonarcloud.io/dashboard?id=es.upm.miw%3Abetca-tpv-user)
Back-end-core | [![Spring Core - Tests](https://github.com/miw-upm/betca-tpv-core/workflows/Spring%20Core%20-%20Tests/badge.svg)](https://github.com/miw-upm/betca-tpv-core/actions) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=es.upm.miw%3Abetca-tpv-core&metric=alert_status)](https://sonarcloud.io/dashboard?id=es.upm.miw%3Abetca-tpv-core) 
Back-end-customer-support | [![Python Customer Support - Tests](https://github.com/miw-upm/betca-tpv-customer-support/workflows/Python%20Customer%20Support%20-%20Tests/badge.svg)](https://github.com/miw-upm/betca-tpv-customer-support/actions) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=es.upm.miw%3Abetca-tpv-customer-support&metric=alert_status)](https://sonarcloud.io/dashboard?id=es.upm.miw%3Abetca-tpv-customer-support)

## :arrow_forward: Aplicación
https://betca-tpv-angular.herokuapp.com/
## :octocat: Repositorios
* [Front-end-angular](https://github.com/miw-upm/betca-tpv-angular)
* [Back-end-user](https://github.com/miw-upm/betca-tpv-user)
* [Back-end-core](https://github.com/miw-upm/betca-tpv-core)
* [Back-end-customer-support](https://github.com/miw-upm/betca-tpv-customer-support)

## :gear: Instalación del proyecto
1. Clonar repositorios, **mediante consola**:

   * betca-tpv-angular
```sh
> cd <folder path>
> git clone https://github.com/miw-upm/betca-tpv-angular
> cd betca-tpv-angular
betca-tpv-angular> npm install
```
   * betca-tpv-user
```sh
> cd <folder path>
> git clone https://github.com/miw-upm/betca-tpv-user
```
   * betca-tpv-core
```sh
> cd <folder path>
> git clone https://github.com/miw-upm/betca-tpv-core
```   

   * betca-tpv-customer-support
```sh
> cd <folder path>
> git clone https://github.com/miw-upm/betca-tpv-customer-support
> cd betca-tpv-customer-support
> venv\Scripts\activate.bat
(venv) > pip install -r requirements.txt
```

2. Importar el proyecto `betca-tpv-angular` mediante **WebStorm** 
   * **Open**, y seleccionar la carpeta del proyecto.
3. Importar los proyectos `betca-tpv-user` & `betca-tpv-core` mediante **IntelliJ** 
   * **Open**, y seleccionar la carpeta del proyecto.
4. Importar el proyecto `betca-tpv-customer-support` mediante **PyCharm**
   * **Open**, y seleccionar la carpeta del proyecto.
5. Ejecución
   * Ejecución de test: se utiliza MongoDB embebido y H2 embebido
   * Ejecución en local:
      1. BBDD. Se debe tener arrancado el motor de MongoDB: `mongodb://localhost:27017/tpv` & `mongodb://localhost:27017/tpv2`,
      y el motor de Postgresql: `spring.datasource.url=jdbc:postgresql://localhost:5432/tpv`
      2. Spring. Ejecutar mediante linea de comando en ambos proyectos: `> mvn spring-boot:run`  
      3. Python. Ejecutar mediante linea de comando: `> uvicorn src.main:app --reload --port 8083`
      4. Angular. Ejecutar mediante linea de comand: `> ng serve`
      5. Navegador. Se arranca en la URL: http://localhost:4200/

# :page_with_curl: Enunciado de la práctica
> La practica consiste en ampliar de forma colaborativa una aplicación web: TPV.  
> **NOTA. Todo el software deberá estar en ingles.**


# :book: Documentación del proyecto
> Este proyecto es la práctica TPV desarrollada de forma colaborativa por todos los alumnos. Se parte de la versión `core`,
ya implementada, y se pretende ampliar con un conjunto de mejoras. Un **T**erminal **P**unto de **V**enta
es un sistema informático que gestiona el proceso de venta mediante una interfaz accesible para los vendedores o compradores.
Permite la creación e impresión del recibo ticket o factura de venta —con los detalles de las referencias y precios— de los artículos vendidos,
actualiza los cambios en el nivel de existencias de mercancías (STOCK) en la base de datos... Además tiene la parte de venta on-line.

## Interfaz de Usuario
* [App TPV desplegada en Heroku](https://betca-tpv-angular.herokuapp.com)

![](./docs/betca-tpv.png)

## Front-end: Angular
### Carpetas
![](docs/front-end-folders.png)
![](docs/front-end-templates.png)
![](docs/front-end-templates-shop.png)
### Módulos
![](docs/front-end-modules.png)
### Seguridad
![](./docs/front-end-security.png)
![](./docs/front-end-routing-security.png)

### Código

#### Uso del Pipe `async`

```html
<p><button mat-raised-button (click)=requestSync() >Sync </button> {{sync}}</p>
<p><button mat-raised-button (click)=requestAsync()>Async</button> {{asyn | async}}</p>
```
```typescript
export class InputOverviewExample {
  sync: string;
  asyn: Observable<string>;
  requestSync(): void {
    this.serviceMock()
    .subscribe(item => this.sync = item);
  }
  requestAsync(): void {
     this.asyn = this.serviceMock();
  }
  serviceMock(): Observable<string> {
    return of('Result');
  }
}
```

### Servicios mock
```typescript
export class ArticleService {
  create(article: Article): Observable<Article> {
    return of(article);
  }
  read(barcode: string): Observable<Article> {
    return of({barcode: barcode, description: '...', retailPrice: 10, providerCompany: 'pro1'})
  }
  search(articleSearch: ArticleSearch): Observable<Article[]> {
    return of([
      {barcode: 123, description: '...', retailPrice: 10, providerCompany: 'pro1'},
      {barcode: 345, description: '...', retailPrice: 10, providerCompany: 'pro2'},
      {barcode: 678, description: '...', retailPrice: 10, providerCompany: 'pro1'}
    ])
  }
```

### Componentes con atributos y eventos
`my-comp.component.html`
```html
<p>Hello {{user}}! <input type="button" value="Ok" (click)="onClick()"></p>
```
```typescript
import { Component, EventEmitter, Input, Output } from '@angular/core';
@Component({ selector: 'app-my-comp', templateUrl: './my-comp.component.html' })
export class MyCompComponent {
   @Input() user = 'By default';
   @Output() pressed = new EventEmitter<string>();
   onClick(){
      this.pressed.emit(this.user)
   }
}
```
`Utilización:`
```html
<app-my-comp></app-my-comp>
<app-my-comp user="Value"></app-my-comp>
<app-my-comp [user]=user></app-my-comp>
<app-my-comp user="With event" (pressed)="onPressed($event)"></app-my-comp>
```

```typescript
export class AppComponent  {
  user = "Variable";
  onPressed(value:string){
    alert(value);
  }
}
```

### Crud Component
```html
<app-crud (create)="create()" (read)="read($event)" (update)="update($event)"
          [data]="articles" [deleteAction]="false" [title]="title"></app-crud>
```
```typescript
export class ArticlesComponent {
  title = 'Articles management';
  articles = of([]);
  create(): void {
    this.dialog.open(ArticleCreationUpdatingDialogComponent);
  }
  read(article: Article): void {
    this.dialog.open(ReadDetailDialogComponent, {
      data: {
        title: 'Article Details',
        object: this.articleService.read(article.barcode)
      }
    });
  }
  update(article: Article): void {
    this.articleService.read(article.barcode)
      .subscribe(fullArticle => this.dialog.open(ArticleCreationUpdatingDialogComponent, {data: fullArticle}));
  }
}
```

---

### Anexo. Preparación del proyecto y ecosistema

#### Instalaciones de herramientas
1. Desinstalar node & borrado de carpetas, si procede:
   * C:\Users\*\AppData\Roaming\npm
   * C:\Users\*\AppData\Roaming\npm-cache

2. Instalar Node, todo estándar
   * node  --version  ?`v16.13.0`
   * npm –version ?`8.1.4`
   * npm install -g npm@8.1.4
   * npm list ?muestra todas las dependencias instaladas
   * npm list &lt;dependence> ?muestra la dependencia especificada
   * npm update –g
   
3. Instalar Angular CLI
   * npm install -g @angular/cli 
   * ng –-version ?`13.0.3`

4. Crear una nueva aplicación
   * ng new &lt;app>. Routing:Y & CSS

5. Ejecutar aplicación:
   * cd &lt;app>
   * ng serve
   * Navegador: http://localhost:4200/
   
6. Instalar express:
   * npm i express  ?i:install
   * npm list express ?`4.17.1`
   * Crear el fichero `server.js`
   * ng build
   * node server.js ?arrancar sobre express
   
7. Instalar Material + Flex
   * ng add @angular/material  ?(Indigo/Pink, Yes & Yes)
   * npm i @angular/flex-layout
   * npm list @angular/material ?`13.0.2`
   * npm list @angular/flex-layout ?`13.0.0-beta.36`
   
8. Instalar Jwt
   * npm i @auth0/angular-jwt
   * npm list @auth0/angular-jwt ?`5.0.2`

Otros comandos
* `>ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.
* `>ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.
* `>ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).
* `>ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).
* `>ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

#### Versionado: **package.json**
```json
{
  "name": "betca-tpv-angular",
  "version": "4.4.0-SNAPSHOT",
}
```
`~: versión mas cercana posible, ^: versión compatible mas alta`
#### Perfil: **carpeta _environments_**

En el fichero `tsconfig`, habilitar las opciones de compilación siguientes, esto nos permite importar valores de los ficheros *.json.
```json
{
  "compilerOptions": {
    "resolveJsonModule": true,
    "esModuleInterop": true,
  }
}
```
`enviroments.ts`
```typescript
import pkg from '../../package.json';
export const environment = {
  production: false,
  NAME: pkg.name,
  VERSION: pkg.version,
  REST_USER: 'http://localhost:8081',
  REST_CORE: 'http://localhost:8082',
  REST_CUSTOMER_SUPPORT: 'http://localhost:8083'
};
```
`enviroments.prod.ts`
```typescript
import pkg from '../../package.json';
export const environment = {
  production: true,
  NAME: pkg.name,
  VERSION: pkg.version,
  REST_USER: 'https://betca-tpv-user.herokuapp.com',
  REST_CORE: 'https://betca-tpv-core.herokuapp.com',
  REST_CUSTOMER_SUPPORT: 'https://betca-tpv-customer-support.herokuapp.com'
```
### Rutas absolutas: @*

En el fichero `tsconfig`, habilitar las opciones de compilación:
```json
{
  "compilerOptions": {
    "baseUrl": "src",
    "paths": {
      "@env": ["environments/environment"],
      "@shared/*": ["app/shared/*"],
      "@core/*": ["app/core/*"]
    }
  }
}
```
### Scripts: **package.json**
```json
{
  "scripts": {
    "heroku-postbuild": "ng build --prod",
    "build-prod": "ng build --prod",
    "start": "node server.js"
  }
}
```
### GitHub Actions: CI & CD
> .gitignore
```typescript
package-lock.json
```
Se establecen los workflows en la carpeta: `.github/workflows/*.yml`

Conexión con **Sonarcloud**:
1. Se debe crear el proyecto en sonarcloud: `Administration/Projects Management`, botón `Create Project`. 

2. Configurar la rama por defecto, renombrar `master` si esta no es la rama por defecto: `Administración/Branches and Pull Requests`.
Renombrar las `long living branch: (master|develop|release-).*`

3. Se deben establecer la contraseña: `secrets.SONAR_TOKEN` en en proyecto de GitHub, `settings/Secrets`
Para `Sonarcloud`, se debe crear el fichero: `sonar-project.properties`.

Conexión con **Heroku**:
1. Crear la aplicación en Heroku.
2. Se deben establecer la contraseña: `secrets.HEROKU_API_KEY` en en proyecto de GitHub.   
3. Deben existir los scripts para construcción y arranque con `express`:
```json
{
  "scripts": {
    "heroku-postbuild": "ng build --prod",
    "start": "node server.js"
  }
}
```

## Back-end: User
> Spring mediante Arquitectura por Capas

### Paquetes
![](docs/back-end-user-packages.png)
### Clases
![](docs/back-end-user-classes.png)
 
## Back-end: Core
> Spring mediante Arquitectura Hexagonal
### Paquetes
![](docs/back-end-core-packages.png)
### Clases
![](docs/back-end-core-classes.png)

## Back-end: Customer Support
> Python mediante Arquitectura Seudo-Hexagonal
### Paquetes
![](docs/back-end-customer-support-packages.png)

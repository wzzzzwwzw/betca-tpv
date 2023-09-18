# Back-end with Open Source Technologies: **SPRING & PYTHON**.
> TPV Project. This project is a teaching support for the subject. It is a complete application made with a Front-end with Angular, 
two Back-ends with Spring and a Back-end with Python. The Back-end-user is developed with synchronous programming and Postgresql. The Back-end-core is
is realized with reactive programming and MongoDB. The Back-end-customer-support with synchronous programming and MongoDB.

## Technologies required
`Java` `Maven` `Spring-Boot` `Reactor` `Python` `Angular` `MongoDB` `JPA` `SQL` `GitHub` `Travis-CI` `Sonarcloud` `Better Code Hub` `Heroku`

## Code status
Project | GitHub - CI | Sonarcloud
-- | -- | --
Front-end-angular | [![Angular - Tests](https://github.com/miw-upm/betca-tpv-angular/actions/workflows/angular-test-sonar.yml/badge.svg)](https://github.com/miw-upm/betca-tpv-angular/actions/workflows/angular-test-sonar.yml) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=es.upm.miw%3Abetca-tpv-angular&metric=alert_status)](https://sonarcloud.io/dashboard?id=es.upm.miw%3Abetca-tpv-angular)
Back-end-user | [![Spring User - Tests](https://github.com/miw-upm/betca-tpv-user/workflows/Spring%20User%20-%20Tests/badge.svg)](https://github.com/miw-upm/betca-tpv-user/actions) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=es.upm.miw%3Abetca-tpv-user&metric=alert_status)](https://sonarcloud.io/dashboard?id=es.upm.miw%3Abetca-tpv-user)
Back-end-core | [![Spring Core - Tests](https://github.com/miw-upm/betca-tpv-core/workflows/Spring%20Core%20-%20Tests/badge.svg)](https://github.com/miw-upm/betca-tpv-core/actions) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=es.upm.miw%3Abetca-tpv-core&metric=alert_status)](https://sonarcloud.io/dashboard?id=es.upm.miw%3Abetca-tpv-core) 
Back-end-customer-support | [![Python Customer Support - Tests](https://github.com/miw-upm/betca-tpv-customer-support/workflows/Python%20Customer%20Support%20-%20Tests/badge.svg)](https://github.com/miw-upm/betca-tpv-customer-support/actions) | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=es.upm.miw%3Abetca-tpv-customer-support&metric=alert_status)](https://sonarcloud.io/dashboard?id=es.upm.miw%3Abetca-tpv-customer-support)

## :arrow_forward: Application
https://betca-tpv-angular.herokuapp.com/
## :octocat: Repositories
* [Front-end-angular](https://github.com/miw-upm/betca-tpv-angular)
* [Back-end-user](https://github.com/miw-upm/betca-tpv-user)
* [Back-end-core](https://github.com/miw-upm/betca-tpv-core)
* [Back-end-customer-support](https://github.com/miw-upm/betca-tpv-customer-support)

## :gear: Project installation
1. Clone repositories, **via console**:

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

2. Import the `betca-tpv-angular` project using **WebStorm**. 
   * **Open**, y seleccionar la carpeta del proyecto.
3. Import `betca-tpv-user` & `betca-tpv-core` projects using **IntelliJ**. 
   * **Open**, and select the project folder.
4. Import the `betca-tpv-customer-support` project using **PyCharm**.
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

# :page_with_curl: Practice statement
> The practice consists of collaboratively extending a web application: POS.  
**NOTE: All software must be in English.


# :book: Documentation of the project
> This project is the TPV practice developed collaboratively by all the students. It is based on the `core` version,
already implemented, and is intended to be extended with a set of enhancements. A **T**Terminal **P**Point of **Sale**Station
is a computer system that manages the sales process through an interface accessible to sellers or buyers.
It allows the creation and printing of the sales receipt or sales invoice - with the details of the references and prices - of the items sold,
updates the changes in the level of stock of goods (STOCK) in the database... It also has an on-line sales part.

## User Interface
* [POS App deployed in Heroku](https://betca-tpv-angular.herokuapp.com)

![](./docs/betca-tpv.png)

## Front-end: Angular
### Folders
![](docs/front-end-folders.png)
![](docs/front-end-templates.png)
![](docs/front-end-templates-shop.png)
### Modules
![](docs/front-end-modules.png)
### Security
![](./docs/front-end-security.png)
![](./docs/front-end-routing-security.png)

### Code

#### Pipe `async` use

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
### mock services
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

### Componentes with attributes and events
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

### Annex. Project preparation and ecosystem

#### Tooling installations
1. Uninstall node & delete folders, if applicable:
   * C:\Users\*\AppData\Roaming\npm
   * C:\Users\*\AppData\Roaming\npm-cache

2. Install Node, all standard
   * node  --version  ?`v16.13.0`
   * npm –version ?`8.1.4`
   * npm install -g npm@8.1.4
   * npm list ?muestra todas las dependencias instaladas
   * npm list &lt;dependence> ?muestra la dependencia especificada
   * npm update –g
   
3. Install Angular CLI
   * npm install -g @angular/cli 
   * ng –-version ?`13.0.3`

4. Create a new application
   * ng new &lt;app>. Routing:Y & CSS

5. Execute application:
   * cd &lt;app>
   * ng serve
   * Navegador: http://localhost:4200/
   
6. Install express:
   * npm i express  ?i:install
   * npm list express ?`4.17.1`
   * Crear el fichero `server.js`
   * ng build
   * node server.js ?arrancar sobre express
   
7. Install Material + Flex
   * ng add @angular/material  ?(Indigo/Pink, Yes & Yes)
   * npm i @angular/flex-layout
   * npm list @angular/material ?`13.0.2`
   * npm list @angular/flex-layout ?`13.0.0-beta.36`
   
8. Install Jwt
   * npm i @auth0/angular-jwt
   * npm list @auth0/angular-jwt ?`5.0.2`

Other commands
* `>ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.
* `>ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.
* `>ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).
* `>ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).
* `>ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

#### Versioned: **package.json**
```json
{
  "name": "betca-tpv-angular",
  "version": "4.4.0-SNAPSHOT",
}
```
`~: closest possible version, ^: highest compatible version`.
#### Profile: **environments of _folder_**.

In the `tsconfig` file, enable the following compilation options, this allows us to import values from *.json files.
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
### Absolute routes: @*

In the `tsconfig` file, enable the compilation options:
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
Workflows are established in the folder: `.github/workflows/*.yml`.

Connection with **Sonarcloud**:
1. The project must be created in sonarcloud: `Administration/Projects Management`, button `Create Project`. 

2. Configure the default branch, rename `master` if this is not the default branch: `Administration/Branches and Pull Requests`.
Rename the `long living branch: (master|develop|release-).*`.

3. Set the password: `secrets.SONAR_TOKEN` in the GitHub project, `settings/Secrets`.
For `Sonarcloud`, create the file: `sonar-project.properties`.

Connection with **Heroku**:
1. Create the application in Heroku.
2. Set the password: `secrets.HEROKU_API_KEY` in the GitHub project.   
3. Scripts for building and starting with `express` must exist:
```json
{
  "scripts": {
    "heroku-postbuild": "ng build --prod",
    "start": "node server.js"
  }
}
```

## Back-end: User
> Spring through Layered Architecture

### Packages
![](docs/back-end-user-packages.png)
### Classes
![](docs/back-end-user-classes.png)
 
## Back-end: Core
> Spring mediante Arquitectura Hexagonal
### Packages
![](docs/back-end-core-packages.png)
### Clases
![](docs/back-end-core-classes.png)

## Back-end: Customer Service
> Python mediante Arquitectura Seudo-Hexagonal
### Packages
![](docs/back-end-customer-support-packages.png)

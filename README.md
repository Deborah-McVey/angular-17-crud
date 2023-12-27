# Angular17Crud

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 17.0.8.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

To be read...,
tutorial from: https://www.bezkoder.com/angular-17-crud-example/ from December 20, 2023. Technology:
Angular 17
RxJS 7
Bootstrap 4
angular 17 globally installed in cmd, project set up in VS Code, VS terminal: cd to folder on my computer create project, cli commands:
ng new angular-17-crud --no-standalone --no-strict --style=css --routing=false ,
Do you want to enable Server-Side Rendering (SSR) and Static Site 
Generation (SSG/Prerendering)? No,
open folder, 
see: no app.routes.ts, no app.config.ts, no app.config.server.ts , 
Bootstrap framework: npm i bootstrap@4.6.2 , angular.json path in styles above styles/css put "../node_modules/bootstrap/dist/css/bootstrap.min.css",
generate models, components, and services listed on tutorial,
include --skip-tests on each generated,
app.module.ts: import FormsModule and 
HttpClientModule, 
add app-routing.module.ts:
define routes,
app.component.html: replace with example text with bootstrap navbar,
app.module.ts: import routeroutlet,
tutorial.model.ts: export class,
tutorial.service.ts: constructor Http, get, create, update, delete, find, 3 methods: getAll(),
deleteAll(),
findByTitle(),
add-tutorial.component.ts (de-bug import paths),
add-tutorial.component.html,
add-tutorial.component.css for submit-form, 
new terminal:
ng s -o,
browser shows black navbar: bezKoder, Tutorial, Add,
child component is tutorial-details,
tutorial-list.component.ts (de-bug import paths), 
tutorials-list.component.html,
tutorial-details.component.ts (incomplete): import OnInit, Input, and Tutorial,
tutorial-list.component.css for list class,
add pagination to tutorial-list component by seeing linked example: ngx-pagination 6,
tutorial-details.component.ts (complete now): debug import paths,
tutorial-details.component.html,
tutorial-details.component.css for edit-form class,
not compiling (problem routerlink) no pagination yet,
npm i ngx-pagination,
app.module.ts: import NgxPaginationModule from 'ngx-pagination',
tutorials-list.component.html: update HTML,
tutorial-list.component.ts: add getRequestParams, update retrieveTutorials, added handlePageChange and handlePageSizeChange,
looked at GitHub sourcecode: https://github.com/bezkoder/angular-17-pagination-example/blob/master/src/app/components/tutorials-list/tutorials-list.component.ts, 
added page, count, pageSize, pagesSizes,
https://github.com/bezkoder/angular-17-pagination-example/blob/master/src/app/components/tutorial-details/tutorial-details.component.html, and ts: still error with routerLink,
app.module.ts:
import AppRoutingModule, removed RouterOutlet,
angular.json:
added scripts paths

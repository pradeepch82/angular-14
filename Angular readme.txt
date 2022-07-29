Features of Angular
====================
1.Dependency Injection
2.Two way data binding
    
3.MVC :
           With angular we can develop application in clean MVC way

4.Testing : Testing is the area where Angular shines really

5.Modules,Directives,Filters/Pipes,Services, Controllers (Components and Templates) etc....

Module is a container for services,directives,pipes,
components and some other modules also.


AngularJS (1.6)                                             Angular (9.0)

1. Not developed by keeping                                 1.Developed specially for
    mobile devlopment in mind.                                Mobile development

2. Basic building block is                                 2.Basic building block is
    Java Script Function                                        a TypeScript class

3.Controllers                                             3.Components and templates

4.filters   (sort,format,search)                          4.pipes (11)

5.services                                                5.providers

6.directives                                              6.directive   
        ng-if                                                        *ngIf
        ng-repeat                                                    *ngFor ,ngModel
      

7.routing   (function based)                              7.routing   (JSON based) 

8.development is easy                                         8.complicated





To make angular development easy Angular team has provided one tool (@angular/cli) 


@angular/cli tool internally depends on Node JS


1.

Install Node JS               :  https://nodejs.org/en/download/
Install Visual Studdion Code  :  https://code.visualstudio.com/


2.node -v

3.npm -v


4.Install angular cli

A.     Local Installation
==========================
     npm i @angular/cli  <enter>

Set Path to Node Js and Angular CLI 

C:\Users\PC5037971>set path=c:\node-v7.10.0-win-x64;c:\angular-cli\node_modules\.bin;

B.     Global Installation
===========================

     npm i -g @angular/cli   <enter>


 To see the version of angular-cli tool
=======================================
  ng version


Create A New Angular Project
===========================
ng new <project-name>

Ex.
D:\angular-12>ng new pvc-angular-app
? Would you like to add Angular routing? Yes
? Which stylesheet format would you like to use? (Use arrow keys)  :CSS
> CSS
  SCSS   [ https://sass-lang.com/documentation/syntax#scss                ]
  Sass   [ https://sass-lang.com/documentation/syntax#the-indented-syntax ]
  Less   [ http://lesscss.org                                             ]



To strat the application
=========================
Go inside the project on command prompt


D:\angular-12\pvc-angular-app>npm start


npm start => ng serve (from package.json)

or 

D:\angular-12\pvc-angular-app>ng serve



npm start => 
        ng serve  =>
                    main.ts =>AppModule
                                =>AppComponent=>
                                           app.component.html=>
                                                        <app-root><app-root>=>index.html




- Generating browser application bundles (phase: setup)...Compiling @angular/core : es2015 as esm2015
Compiling @angular/common : es2015 as esm2015
Compiling @angular/platform-browser : es2015 as esm2015
Compiling @angular/router : es2015 as esm2015
Compiling @angular/platform-browser-dynamic : es2015 as esm2015
√ Browser application bundle generation complete.

Initial Chunk Files   | Names         |      Size
vendor.js             | vendor        |   2.38 MB
polyfills.js          | polyfills     | 508.83 kB
styles.css, styles.js | styles        | 381.01 kB
main.js               | main          |  57.39 kB
runtime.js            | runtime       |   6.58 kB

                      | Initial Total |   3.32 MB

Build at: 2021-07-03T05:28:05.207Z - Hash: 1014fc027562cbfbd9c0 - Time: 53930ms

** Angular Live Development Server is listening on localhost:4200, open your browser on http://localhost:4200/ **


√ Compiled successfully.
√ Browser application bundle generation complete.

5 unchanged chunks

Build at: 2021-07-03T05:28:08.147Z - Hash: 4cac0456c5a66e4beb22 - Time: 2175ms

√ Compiled successfully.


angular cli commands
=========================

To create a component  => ng g c  <Angular4Basics>
To create a service    => ng g s  <AngularService>
To create a directive  => ng g d  <AngularDirective>
To create a pipe       => ng g p  <AngularPipe>
To create a module     => ng g m  <AngularModule>
To create a class      => ng g class <AngularClass>


Routing
===========
/basics        => AngularBasics
/pipes         => AngularPipes
/technologies  => Technologies
/home          => Home  


templateUrl: './app.component.html',//Where to display if code is greater than 3 lines

template: '<h2>{{title}}</h2>',//Where to display if code is leass than 4 lines


Component is responsible for 4 things

 1.What to display?
 2.How to display?
 3.Where to display?
 4.Where to inject?


Angular Binding types
======================

1. Interpolation   

       Interpolation use the {{ expression }} to render the bound value to the component’s template.

2.Property Binding

       Property binding user [] to send values from the component  to the template.

3.Event Binding

         (click)="showHide()"

4.One way data binding
         
           [ngModel]="name"

4.Two way data binding
         
           [(ngModel)]="name"
     


 

Note :TypeScript class members are public by default.

comopnent  ->@Component
module     ->@NgModule
pipe       ->@Pipe
directive  ->@Directive
service    ->@Injectable


Angular Directives  : add functionalities to HTML elements
==========================================================

Attribute Directve    :Won't change the HTML DOM structure
====================== 
 [ngStyle]
 [ngClass]
 [ngModel] =>It is applicable for only input elements > FormsModule
 [ngSwitch]


Structural Directive :Will change the HTML DOM structure
====================
   *ngFor
   *ngIf
   *ngSwitchCase   => It is applicable for only container tags
   *ngSwitchDefault=> It is applicable for only container tags

Component Directive
==================
<app-root>  </app-root>
<ng-template></ng-template>
<router-outlet><router-outlet>


2.Custom Directives
=======================
Attribute Directive   :  ElementRef and Renderer2
====================

<h1  [bgColor]="'red'"  [fgColor]="'red'" >Hello World</h1>

Structural Directive    :TemplateRef  and VieContainerRef
=======================

<h1  *show="true">Hello World</h1>

<h1  *hide="true">Hello World</h1>



Day2  :
======
Angular Pipes & Services

Angular Pipes are used to format ,sort search (filter) the data.

Angular Buitlin Pipes
======================

String
========
uppercase
lowercase
titlecase (angular4)
slice  

array
=====
slice

array|slice:startIndex:lastIndex


number
======
number     salary|number:'9.3-4'   
currency   salary|currency:'Rs'
percent    salary|percent

date
=====
date      

dob|date:'shortDate'
dob|date:'mediumDate'
dob|date:'longDate'
dob|date:'fullDate'
dob|date:'dd-MM-yyyy'

Object
======
object|json
object|keyvalue

Observable
===========
async


Angular Custom Pipes
=====================
gender|gender      :1=>Male ,2=>Female, 3=>Not disclosed


gender|title    =>       gender=1 and isMarried=false      => Mr.
                                 gender=1 and isMarried=true       =>  Mr. 
                                 gender=2 and isMarried=false     =>  Miss
                                 gender=2 and isMarried=true      =>   Mrs.



employees|orderBy   =>       sort employees on id basis in ascending order

employees|orderBy:'id'   =>sort employees on id basis in ascending order

employees|orderBy:'name'   =>sort employees on name basis in ascending order

employees|orderBy:'name':true   =>sort employees on name basis in descending order


array.sort((e1,e2)=>e1.id-e2.id);
     =>


array.sort(function(e1,e2){
return e1.id-e2.id;
})


employees|filter:'searchText'


Install ng2-search-filter Package

   npm i ng2-search-filter


Import Ng2SearchPipeModule in AppModule

import {Ng2SearchPipeModule} from "ng2-search-filter";


Implementing Search Filter in Angular Component

employees|filter:'searchText'

Run Development Server



Angular Application to perform CRUD operations



dummy data
============
 employees=[
    {id:12,name:'Ram chinchole',salary:2345500,variable:0.15,
    city:'Pune',mobile:'8149976894',pan:'cmxac9845d',
    doj:new Date("February 01,2011"),isMarried:true,gender:1,age:33
   },
   {id:23,name:'Sachin chinchole',salary:324242.456784343,variable:0.10,
   city:'Mumbai',mobile:'7123456732',pan:'abxac9845a',
   doj:new Date("April 01,2013"),isMarried:true,gender:1,age:23
  },
  
  {id:11,name:'Ameya Joshi',salary:34343.456784343,variable:0.11,
  city:'Mumbai',mobile:'7788554433',pan:'abcac9845c',
  doj:new Date("June 01,2018"),isMarried:true,gender:1,age:34
 },
 
 {id:14,name:'Prachitee chinchole',salary:45345.456784343,variable:0.20,
 city:'Pune',mobile:'9158652627',pan:'xyzac9845d',age:45,
 doj:new Date("June 01,2010"),isMarried:false,gender:2
},

{id:21,name:'Prachi chinchole',salary:4345345.456784343,variable:0.15,
city:'Solapur',mobile:'9890732222',pan:'pvcac9845d',age:56,
doj:new Date("February 01,2017"),isMarried:true,gender:2
},

{id:17,name:'Mahesh chinchole',salary:345345.34324,variable:0.12,
city:'Solapur',mobile:'7158652622',pan:'amxac9845d',
doj:new Date("May 01,2013"),isMarried:false,gender:3,age:25
},

];

day3
=====
Angular Services  (Reusbale business logic)
===============================================

Angular provides builtin HttpClient service available in  HttpClientModule  (@angular/common/http) to invoke remote service.


Fake Restful Web API
========================

https://jsonplaceholder.typicode.com/users            GET
https://jsonplaceholder.typicode.com/users/1          GET

https://jsonplaceholder.typicode.com/posts
https://jsonplaceholder.typicode.com/posts/1
https://jsonplaceholder.typicode.com/posts?userId=1


https://jsonplaceholder.typicode.com/comments
https://jsonplaceholder.typicode.com/comments/1
https://jsonplaceholder.typicode.com/comments?postId=1


https://jsonplaceholder.typicode.com/todos
https://jsonplaceholder.typicode.com/todos/1
https://jsonplaceholder.typicode.com/todos?userId=1


https://jsonplaceholder.typicode.com/albums
https://jsonplaceholder.typicode.com/albums/1
https://jsonplaceholder.typicode.com/albums?userId=1


https://jsonplaceholder.typicode.com/photos
https://jsonplaceholder.typicode.com/photos/1
https://jsonplaceholder.typicode.com/photos?albumId=1





5.RouteParams and QueryParams
=============================

Use ActivatedRoute class to retrieve route params and query params


constructor(private us:UsersService,private route:ActivatedRoute) { 
    console.log("#######  UsersComponent created  ########");
  }


Route Param/PathParam/PathVariable
==================================

https://jsonplaceholder.typicode.com/users/1
https://jsonplaceholder.typicode.com/posts/1
https://jsonplaceholder.typicode.com/todos/1
https://jsonplaceholder.typicode.com/albums/1
https://jsonplaceholder.typicode.com/photos/1



       {path:'users/:userId',component:UsersComponent},


        syntax:    this.userId=this.route.snapshot.params.userId;

QueryParams/QueryString
============

https://jsonplaceholder.typicode.com/posts?userId=1
https://jsonplaceholder.typicode.com/albums?userId=1
https://jsonplaceholder.typicode.com/todos?userId=1
https://jsonplaceholder.typicode.com/comments?postId=1


 syntax  :  this.userId=this.route.snapshot.queryParams.userId;


Module level service

=====================
From Angular 5
------------------------------------
@Injectable({
  providedIn: 'root'
})
export class UsersService {
  constructor() { }
}


Before Angular 5
---------------------------------------------------
@Injectable()
export class UsersService {
  constructor() { }
}


import { UsersService } from './services/users.service';
@NgModule({
providers: [UsersService],
  bootstrap: [AppComponent]
})
export class AppModule { }


Component Level Service
-----------------------------------


















day4 :17-July-2021
====

1.NestedComponent(Parent child Communcation)

Parent -> child   => @Input()

Child ->   Parent  =>  @Output()  =>EventEmitter
     


Country
        name=""
       stateName=""
       cityName="" 
        
       State
          name=""
          countryName=""
          cityName=""

             City
                 name=""    
                 countryName=""
                 stateName=""










 
 day5   18-July-2021
 =====


3.FormValidation
=================
1.Template Driven Forms
2.Reactive Forms/Model Driven Form 

Template Driven Forms Features
===============================
Easy to use
Suitable for simple scenarios and fails for complex scenarios
Similar to AngularJS
Two way data binding(using [(NgModel)] syntax)
Minimal component code
Automatic track of the form and its data(handled by Angular)
Unit testing is another challenge


Reactive Forms Features
===========================================
More flexible, but needs a lot of practice
Handles any complex scenarios
No data binding is done (immutable data model preferred by most developers)
More component code and less HTML markup
Reactive transformations can be made possible such as
Handling a event based on a debounce time
Handling events when the components are distinct until changed
Adding elements dynamically
Easier unit testing


FormGroup,FormBuilder,Validators => ReactiveFormsModule




4.Pagination
=================


5.RouteParams and QueryParams
=============================

Use ActivatedRoute class to retrieve route params and query params


constructor(private us:UsersService,private route:ActivatedRoute) { 
    console.log("#######  UsersComponent created  ########");
  }


Route Param
===========


https://jsonplaceholder.typicode.com/users/1

       {path:'users/:userId',component:UsersComponent},


        syntax:    this.userId=this.route.snapshot.params.userId;

QueryParams
============

https://jsonplaceholder.typicode.com/posts?userId=1

   syntax  :  this.userId=this.route.snapshot.queryParams.userId;


@ViewChild
===========

1.To Inject The Component

   @ViewChild(NumberComponent,{static:false}) 
  private n:NumberComponent; 


2.To Inject The Directive


  @ViewChild(FgColorDirective,{static:false}) 
  private f:FgColorDirective;
  

3.To Inject The ElementRef

  @ViewChild("name",{static:false}) 
  private name:ElementRef;
  
  @ViewChild("city",{static:false}) 
  private city:ElementRef;
  

day5   24-July-2021
=====

Angular Gurads
===============
The Angular router’s navigation guards allow to grant or remove access to certain parts of the navigation.
Note that client-side route guards like this are not meant to be a security feature. 
They won't prevent a clever user from figuring out a way to get to the protected routes. 
Such security should be implemented on the server. They are instead meant as a way to improve the UX for your apps.

Types of Guards
================
1.CanActivate:
	 Controls if a route can be activated.

2.CanActivateChild:
	 Controls if children of a route can be activated.

3.CanLoad: 
	Controls if a route can even be loaded. This becomes useful for feature modules
	that are lazy loaded. They won’t even load if the guard returns false.

4.CanDeactivate: 
	Controls if the user can leave a route. Note that this guard doesn’t prevent the
	user from closing the browser tab or navigating to a different address. 
	It only prevents actions from within the application itself.



To create guard
================

ng g guard guards/Multi


import { Injectable } from '@angular/core';
import { ActivatedRouteSnapshot, CanActivate, CanActivateChild, CanDeactivate, CanLoad, Route, Router, RouterStateSnapshot, UrlSegment, UrlTree } from '@angular/router';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class MultiGuard implements CanActivate, CanActivateChild, CanDeactivate<unknown>, CanLoad {
 
 
  constructor(private router:Router){
    console.log("=============MultiGuard created=======");
    
  }

 
  canActivate(
    route: ActivatedRouteSnapshot,
    state: RouterStateSnapshot): Observable<boolean | UrlTree> | Promise<boolean | UrlTree> | boolean | UrlTree {
    
      var email=sessionStorage.getItem("email");

      if(email==null ||email==undefined)
      {
        alert("Login First");
        this.router.navigate(["/login"]);
        return false;

      }    
      return true;

  }
 
 
  canActivateChild(
    childRoute: ActivatedRouteSnapshot,
    state: RouterStateSnapshot): Observable<boolean | UrlTree> | Promise<boolean | UrlTree> | boolean | UrlTree {
    
      var email=sessionStorage.getItem("email");

      if(email!="pradeep@gmail.com")
      {
        alert("You are not authorized to visit this section ,try with other credentials");
        this.router.navigate(["/login"]);
        return false;
      }    
      return true;

  }
 
 
  canDeactivate(
    component: unknown,
    currentRoute: ActivatedRouteSnapshot,
    currentState: RouterStateSnapshot,
    nextState?: RouterStateSnapshot): Observable<boolean | UrlTree> | Promise<boolean | UrlTree> | boolean | UrlTree {
    
    return confirm("Do you want to leave this Page?");
  }
 
 
  canLoad(
    route: Route,
    segments: UrlSegment[]): Observable<boolean | UrlTree> | Promise<boolean | UrlTree> | boolean | UrlTree {
    
      return confirm("Do you want to load this Address Module?");
 
  }
}

Guard Registration with routes
===================================

app.routing.module.ts
=======================

const routes: Routes = [
  {path:'home',component:HomeComponent,canActivate:[MultiGuard]},
  {path:'basics',component:AngularBasicsComponent,canActivate:[MultiGuard]},
  {path:'pipes',component:AngularPipesComponent,canActivate:[MultiGuard]},
  {path:'technologies',component:TechnologiesComponent,canActivate:[MultiGuard]},
  {path:'customdirectives',component:CustomDirectivesComponent,canActivate:[MultiGuard]},
  {path:'nested',component:NestedComponent,canActivate:[MultiGuard],canDeactivate:[MultiGuard]},
  {path:'viewchild',component:ViewchildComponent,canActivate:[MultiGuard],canDeactivate:[MultiGuard]},
  {path:'login',component:LoginComponent},
  {path:'register',component:RegisterComponent},
  {path:'address',loadChildren:()=>import ("./address/address.module").then(mod=>mod.AddressModule),canLoad:[MultiGuard]},
    
  {path:'customers',component:CustomersComponent,canActivate:[MultiGuard]},
  
  
  
  {path:'casestudy',component:CaseStudyComponent,canActivate:[MultiGuard],canActivateChild:[MultiGuard],
  children:[
  {path:'users',component:UsersComponent,
  children:[
    {path:'list',component:UsersListComponent},
    {path:'table',component:UsersTableComponent},
  ]

},
  {path:'users/:userId',component:UsersComponent},
  {path:'posts',component:PostsComponent},
  {path:'comments',component:CommentsComponent},
  {path:'todos',component:TodosComponent},
  {path:'albums',component:AlbumsComponent},
  {path:'photos',component:PhotosComponent},
  ]
},
 

  {path:'**',redirectTo:"home"},
  ];


Angular Comonent LifeCycle  Hooks
===================================

import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-parent',
  templateUrl: './parent.component.html',
  styleUrls: ['./parent.component.css']
})
export class ParentComponent implements OnInit {

  message="Hello Students!!!";


  childMessage="";


  
  constructor() {
    console.log("$$$$$$$$$$$$$$$$$$ ParentComponent created   $$$$$$$$$$")
   }

  ngOnInit() {
    console.log("$$$$$$$$$$$$$$$$$$ ParentComponent initialized   $$$$$$$$$$")
  }
  
  ngOnDestroy() {
    console.log("$$$$$$$$$$$$$$$$$$ ParentComponent destroyed  $$$$$$$$$$")
   
  }
  
  ngOnChanges() {
    console.log("$$$$$$$$$$$$$$$$$$ ParentComponent ngOnChanges  $$$$$$$$$$")
  }
  
  ngAfterContentInit() {
    console.log("$$$$$$$$$$$$$$$$$$ ParentComponent ngAfterContentInit  $$$$$$$$$$")
  }
  
  ngAfterContentChecked() {
    console.log("$$$$$$$$$$$$$$$$$$ ParentComponent ngAfterContentChecked  $$$$$$$$$$")
  }
  
  ngAfterViewChecked() {
    console.log("$$$$$$$$$$$$$$$$$$ ParentComponent ngAfterViewChecked  $$$$$$$$$$")
  }
  
  ngAfterViewInit() {
    console.log("$$$$$$$$$$$$$$$$$$ ParentComponent ngAfterViewInit  $$$$$$$$$$")
  }


}





day7   31-July-2021
=====
Angular Configuration
=====================

angular.json
tsconf.json


Angular Testing
=================
ng new project --skip-tests

ng g c A --skip-tests=true
ng g s A --skip-tests=true
ng g p A --skip-tests=true
ng g d A --skip-tests=true


ng test

Jasmin is api  : to write test or TestSuite

it()         -unit test
describe()   -Test Suite


xit()         -skip unit test
xdescribe()   -skip Test Suite


Karma : Test Runner  : karma.conf.js : 9876

app :3
A   :1
B   :1

CalculatorService :6



Angular Production Code 
========================
Before Angular 9  : ng build --prod

From Angular 9    : ng build

1.It  will genrate dist/app-name/
2.Copy all html ,css,js files in backend application


Angular Readymade CaseStudy
===============================

https://github.com/DanWahlin/Angular-JumpStart

Angular + Express  (You need to convert in Backend -Spring Boot)



To run Backend : node server.js  or npm start    http://localhost:8080

To run Front   : ng serve    http://localhost:4200


or
===

ng build 

node server.js

http://localhost:8080


Angular + Spring Boot

4200    +  1212  

CORS Policy : Cross Origin Resource Sharing

1. Caller and Callee  shoud use same domain
2. Caller and Callee  shoud use same protocol
3. Caller and Callee  shoud use same port















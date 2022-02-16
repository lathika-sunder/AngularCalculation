
# AngularCalculation

# Web Page for Mathematical Calculations using Angular

## AIM:
To design a dynamic website to perform mathematical calculations using Angular Framwork

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS in component.html file

### Step 3:

Write typescript to perform the calculations.

### Step 4:

Validate the layout in various browsers.

### Step 5:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
app.component.html coding:
~~~
<body>
    <h1>Math Calculations</h1>
    <div class="container">
    <div class="content">
    <app-rectangle></app-rectangle>
    <div class="footer">Developed By Lathika Sunder</div>
    </div>
    <div class="content">
    <app-cone></app-cone>
    <div class="footer">Developed By Lathika Sunder</div>
    </div>
    </div>
    </body>
~~~
app.component.css coding:
~~~
{
    box-sizing:border-box;
    font-family: Arial, Helvetica, sans-serif;
  }
  body {
    background-color:rgb(0, 0, 0);
  }
  .container {
    width:1080px;
    margin-left: auto;
    margin-right: auto;
    padding-left: 300px;
    max-height:max-content;
    background-color:rgb(77, 231, 5);
    padding-bottom: 45px; ;
  }
  .content {
    display:block;
    width: 500px;
    background-color:rgb(236, 79, 215);
    min-height: 150px;
    font-size: 20px;
    position:relative;
    
  }
  h1{
    text-align: center;
    color:black;
  }
  
  .footer {
    display: inline-block;
    width: 100%;
    height: 40px;
    background-color:rgb(212, 34, 212);
    text-align:right;
    padding-top: 30px;
    margin: 0px 0px 0px 0px;
    color: #000000;
  }
~~~
app.component.ts coding:
~~~
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'mathcalculations';
}
~~~
square.component.html coding:
~~~
<h2>Area of a Square</h2>
    <div class="formelement">
    Length=<input type="text" [(ngModel)]="length"> Meters <br/>
    </div>
    <div class="formelement">
    Length=<input type="text" [(ngModel)]="length"> Meters <br/>
    </div>
    <div class="formelement">
        <input type="button" (click)="onCalculate()" value="Calculate Area"> <br/>
    </div>
    <div class="formelement">
    Area=<input type="text" [value]="area"> Meters<sup>2</sup>
    </div>
~~~
square.component.css coding:
~~~
 {
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
  }
  .container {
    width: 1080px;
    margin-left: auto;
    margin-right: auto;
    padding-top: 30px;
    padding-left: 300px;
    padding-bottom: 500px;
  }
  .content {
    display:block;
    width: 500px;
    background-color:rgb(231, 13, 13);
    min-height: 150px;
    font-size: 20px;
  }
  h2{
      text-align: center;
      padding-top: 25px;
  }
  .formelement{
      text-align: center;
      margin-top: 5px;
      margin-bottom: 5px;
  }
~~~
square.component.ts coding:
~~~
import { Component } from "@angular/core"

@Component({
    selector: 'app-rectangle',
    templateUrl:'./rectangle.component.html',
    styleUrls:['./rectangle.component.css']
})
export class RectangleComponent{
    length:number;
    area:number;
    constructor(){
        this.length=0;
        this.length=0;
        this.area =this.length * this.length;

    }
    onCalculate()
    {
        this.area =  this.length * this.length;
    }
}
~~~
cone.component.html coding:
~~~
<h2>Volume of a Cone</h2>
<div class="formelement">
Radius=<input type="text" [(ngModel)]="radius"> Meters <br/>
</div>

<div class="formelement">
    <input type="button" (click)="onCalculate()" value="Calculate Volume"> <br/>
</div>
<div class="formelement">
Volume=<input type="text" [value]="volume"> Meters<sup>3</sup>
</div>
~~~
cone.component.css coding:
~~~
* {
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
  }
  h2{
      text-align: center;
      padding-top: 25px;
  }
  .formelement{
      text-align: center;
      margin-top: 5px;
      margin-bottom: 5px;
  }
~~~
cone.component.ts coding:
~~~
import { style } from "@angular/animations";
import { Component } from "@angular/core"

@Component({
    selector: 'app-cone',
    templateUrl:'./cone.component.html',
    styleUrls:['./cone.component.css']

})
export class ConeComponent{
    radius:number;
    
    volume:number;
    constructor(){
        this.radius=0;
        this.volume = 3.14 * this.radius * this.radius * this.radius * 1.33;
        
    }
    onCalculate()
    {
        this.volume = 3.14 * this.radius * this.radius * this.radius * 1.33;
    }
}
~~~
app.module.ts coding:
~~~
import { NgModule } from '@angular/core';
import { FormsModule } from '@angular/forms';
import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component';
//import { RectangleComponent } from './rectangle/rectangle.component';
import { ConeComponent } from './cone.component';
//import { ConeComponent } from './cone/cone.component';
//import { RectangleComponent } from './Rectangle/Rectangle.component';
import { RectangleComponent } from './rectangle.component';
//import { RectangleComponent } from './rectangule/rectangule.component';


@NgModule({
  declarations: [
    AppComponent,RectangleComponent,ConeComponent
  ],
  imports: [
    BrowserModule,FormsModule,
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
~~~


## OUTPUT:
![output](./t.jpeg)


## Result:
A dynamic website to perform mathematical calculations using Angular Framwork has been designed.
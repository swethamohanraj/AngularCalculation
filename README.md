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
```
HTML(app.component.html):
 <style>
    * {
      box-sizing: border-box;
      font-family: Arial, Helvetica, sans-serif;
    }
    body {
      background-color: #880cee
    }
    .container {
      width: 1080px;
      margin-left: auto;
      margin-right: auto;
    }
    .contentrec {
      display: block;
      width: 100%;
      background-color: rgb(85, 221, 126);
      min-height: 500px;
      margin-top:150px
    }
    .contentcy {
      display: block;
      width: 100%;
      background-color: rgb(241, 232, 100);
      min-height: 500px;
      margin-top:150px
    }
    .contentcu {
      display: block;
      width: 100%;
      background-color: #f49fff;
      min-height: 500px;
      margin-top:150px
    }
    h1{
        text-align: center;
        padding-top: 20px ;
    }
    .formelement{
        text-align: center;
        line-height: 200%;
        margin: auto;
        padding: 10px;
        font-size: 20px;


    }
    .formelementV{
        text-align: center;
        margin: auto;
        padding: 10px;
        font-size: 20px;
        line-height: 200%;
    }

    .footer {
display: block;
width: 100%;
height: 40px;
background-color:  cyan;
text-align: center;
padding-top: 10px;
margin: 0px 0px 0px 0px;
color:purple;
}
        </style>
    <body>
<h1>MATHEMATICAL CALCULATIONS</h1>

<div class="container">
    <div class="contentrec">
      
<Rectangle-Area class="formelement"></Rectangle-Area>
</div>
</div>


<div class="container">
    <div class="contentcy">

<Cylinder-Volume class="formelementV"></Cylinder-Volume>
</div>
</div>

<div class="container">
    <div class="contentcu">
<Cuboid-Volume class="formelementV"></Cuboid-Volume>
</div>
</div>
<div class="footer">
    Developed by Sowmiya.
 </div>
</body>
TS(app.component.ts):
import { NgModule } from '@angular/core';
import { FormsModule } from '@angular/forms';
import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component';
import { CuboidComponent } from './cuboid/cuboid.component';
import { CylinderComponent } from './cylinder/cylinder.component';
import { RectangleComponent } from './rectangle/rectangle.component';

@NgModule({
  declarations: [
    AppComponent,RectangleComponent,CylinderComponent,CuboidComponent
  ],
  imports: [
    BrowserModule,FormsModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
Calculation 1 - Area of Rectangle:
HTML File:
<div>
    <h2>Area of a Rectangle</h2>
    Length = <input type="text" [(ngModel)]="length"> Meters<br/>
    Breadth = <input type="text" [(ngModel)]="breadth"> Meters<br/>
       <input type="button" (click)="onCalculation()" value="Calculate Area"><br/>
    Area of Rectangle = <input type="text" [value]="area"> Meters<sup>2</sup>
</div>
TS File:
import { Component } from "@angular/core";

@Component({
    selector :" Rectangle-Area ",
    templateUrl:"./rectangle.component.html"
})

export class RectangleComponent{
    length:number;
    breadth:number;
    area:number;
    constructor(){
        this.length=10;
        this.breadth=20;
        this.area= this.length * this.breadth;

    }
    onCalculation()
    {
        this.area= this.length * this.breadth;
    }
}
Calculation 2 - Volume of Cylinder:
HTML File:
<div>
    <h2>Volume of Cylinder</h2>
    Radius = <input type="text" [(ngModel)]="radius"  > Meters<br/>
    Height = <input type="text" [(ngModel)]="height"> Meters<br/>
       <input type="button" (click)="onCalculateVolume()" value="Calculate Volume"><br/>
    Volume of Cylinder = <input type="text" [value]="volume"> Meters<sup>3</sup>
</div>
TS File:
import { Component } from "@angular/core";

@Component({
    selector :" Cylinder-Volume ",
    templateUrl:"./cylinder.component.html"
})

export class CylinderComponent{
    radius:number;
    height:number;
    volume:number;
    constructor(){
        this.radius=10;
        this.height=20;
        this.volume= 3.14*this.radius*this.radius * this.height;

    }
    onCalculateVolume()
    {
        this.volume= 3.14*this.radius*this.radius * this.height;
    }
}
Calculation 3 - Volume of Cuboid:
HTML File:
<div>
    <h2>Volume of Cuboid</h2>
    Length= <input type="text" [(ngModel)]="length"  > Meters<br/>
    Height = <input type="text" [(ngModel)]="height"> Meters<br/>
    Width = <input type="text" [(ngModel)]="width"> Meters<br/>
       <input type="button" (click)="onCalculateVolumecuboid()" value="Calculate Volume"><br/>
    Volume of Cuboid = <input type="text" [value]="volume"> Meters<sup>3</sup>
</div>
TS File:
import { Component } from "@angular/core";

@Component({
    selector :" Cuboid-Volume ",
    templateUrl:"./cuboid.component.html"
})

export class CuboidComponent{
    length:number;
    height:number;
    width:number;
    volume:number;
    constructor(){
        this.length=10;
        this.height=20;
        this.width=15;
        this.volume= this.length*this.height*this.width

    }
    onCalculateVolumecuboid()
    {
        this.volume= this.length*this.height*this.width
    }
}
```
## OUTPUT:
![1](https://user-images.githubusercontent.com/94228215/153768012-b11b0a8c-8758-4d93-ac06-bdb484613804.jpeg)

![2](https://user-images.githubusercontent.com/94228215/153768022-d27b8b1e-3777-45e9-ac74-80551164898d.jpeg)

![3](https://user-images.githubusercontent.com/94228215/153768039-01f96ba5-6b3b-48bb-9254-73c54e24e49d.jpeg)

![4](https://user-images.githubusercontent.com/94228215/153768060-0f48ace0-d5f3-4b5b-b2cd-db5c4c85da15.jpeg)


## Result:
A dynamic website to perform mathematical calculations using Angular Framwork is designed.

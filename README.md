# Angular Workshop: Initial-Setup

## 1. Development Environment  

Before getting started, set up your development environment by installing the following tools:  

1. [Node.js](https://nodejs.org/en)  
2. [Visual Studio Code](https://code.visualstudio.com)  
3. [Angular Essentials (John Papa)](https://marketplace.visualstudio.com/items?itemName=johnpapa.angular-essentials)  
4. [Tailwind CSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)  
5. [Google Chrome](https://www.google.com/intl/de_de/chrome/)  
6. [Angular DevTools](https://chromewebstore.google.com/detail/angular-devtools/ienfalfjdbdpebioblfackkekamfmbnh)  
7. Angular CLI: Install via  `npm install -g @angular/cli`

## 2. Project Setup  

To set up your Angular project, follow these steps:  

1. Create a new Angular project by running `ng new clash`.  
2. Navigate into the project directory with `cd clash`.  
3. Open the project in Visual Studio Code using `code .`.  
4. Start the development server by running `npm start`.  
5. Clean up the `app.component.html` file to remove default content.  

## 3. Install Tailwind CSS with Angular  

Follow the official guide to install Tailwind CSS with Angular:  
[https://tailwindcss.com/docs/installation/framework-guides/angular](https://tailwindcss.com/docs/installation/framework-guides/angular)

## 4. Your first test

1. Create a file **app.component.spec.ts** next to the **app.component.ts** with the following content:
```ts
import { ComponentFixture, TestBed, waitForAsync } from '@angular/core/testing';
import { AppComponent } from './app.component';

describe('AppComponent', () => {
  let component: AppComponent;
  let fixture: ComponentFixture<AppComponent>;

  beforeEach(waitForAsync(() => {
    TestBed.configureTestingModule({
      imports: [AppComponent],
    }).compileComponents();
  }));

  beforeEach(() => {
    fixture = TestBed.createComponent(AppComponent);
    component = fixture.componentInstance;
    fixture.detectChanges();
  });

  it('should create', () => {
    expect(component).toBeDefined();
  });

  it('should render "Hello Workshop" in a h1 tag', () => {
    const compiled = fixture.nativeElement;
    expect(compiled.querySelector('h1').textContent).toContain(
      'Hello Workshop'
    );
  });
});
```
2. Run the test `npm run test`
4. Fullfill the test





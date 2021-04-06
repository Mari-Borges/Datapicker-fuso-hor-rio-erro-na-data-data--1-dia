# Sobre

Este projeto foi feito para entender sobre o matDatapicker

Sobre o modo que é tratado o fuso horário em anguns casos o a data aparece com -1 dia

Isso acontece por falta de algumas contigurações no providers
 
 Então só é preciso acrescentar o que falta: no exemplo abaixo esta como estava o meu projeto antes, enquanto estava dando o erro: 
 providers: [
    { provide: MAT_DATE_FORMATS, useValue: MY_FORMATS },
    ]

Este exemplo é de como ficou depois de acrescentar algumas coisas, e apareceu a hora correta:

 providers: [
    { provide: MAT_DATE_LOCALE, useValue: 'ru-RU' },
    { provide: MAT_DATE_FORMATS, useValue: MY_FORMATS },
    { provide: DateAdapter, useClass: MomentDateAdapter },
    { provide: MAT_MOMENT_DATE_ADAPTER_OPTIONS, useValue: { useUtc: true } }
    ]



# MatDateP

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.2.7.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

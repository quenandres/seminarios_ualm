<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="200" alt="Nest Logo" /></a>
</p>

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

### `SeminarioTesting`

*https://ualmtorres.github.io/SeminarioTesting/*

```ts
it( // Definicion de la prueba
  'should return "Hello World!"', //Nombre del caso de prueba
  () => { // Funciona de evaluacion del test con la definicion de las espectativas
    expect(appController.getHello()).toBe('Hello World!'); // se usa para comprobar un valor obtenido por una funcion matcher como toBe.
  }
);
```


_*describe*_ Nos proporsiona la opción de agrupar varios test en un mismo archivo
```ts
describe('root', () => { 
    it('should return "Hello World!"', () => { 
      expect(appController.getHello()).toBe('Hello World!');
    });

    it('should ....' () => { 
      // test code
    });
  });
```
Esta función forma parte del conjunto de funciones de preparación o limpieza del entorno de testing:

_*beforeAll*_ se ejecuta una sola vez antes de todos los tests del bloque.

_*beforeEach*_ se ejecuta antes de cada test del bloque.

_*afterEach*_ se ejecuta después de cada test del bloque.

_*afterAll*_ se ejecuta una sola vez después de todos los tests del bloque.
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
it(// Definicion de la prueba
'should return "Hello World!"', () => { //Nombre del caso de prueba
  // Funciona de evaluacion del test con la definicion de las espectativas
  expect(appController.getHello()).toBe('Hello World!'); // se usa para comprobar un valor obtenido por una funcion matcher como toBe.
});
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

### `2.3. Implementación de la kata Fizz Buzz`

Se crea metodo en el servicio, se crea la ruta fizzbuzz en el controlador

### `2.4. Pruebas unitarias del servicio`

### `2.5. Cobertura de tests`

La cobertura de test nos muestra el porcentaje de lineas que se estan probando.

Cambiar el comando, al agregarle --verbose, mostraremos los test mas especificados.

```js
"test": "jest --verbose",
```

Mantendremos la consola activada para que ejecute los test cada cambio.

```bash
npm run test:watch
```

Esto ejecutará los tests nos dará el porcentaje de código testado para cada archivo y a nivel global.

```bash
npm run test:cov
```

### `2.5.1. Exclusión de archivos de la cobertura de tests`

Si queremos ignorar todos los modulos (_*module.ts*_) agregamos el elemento en el _coveragePathIgnorePatterns_ para excluir estos archivos.

```json
"jest": {
    "moduleFileExtensions": [
      "js",
      "json",
      "ts"
    ],
    "rootDir": "src",
    "testRegex": ".*\\.spec\\.ts$",
    "transform": {
      "^.+\\.(t|j)s$": "ts-jest"
    },
    "collectCoverageFrom": [
      "**/*.(t|j)s"
    ],
    "coverageDirectory": "../coverage",
    "coveragePathIgnorePatterns": [".module.ts"],
    "testEnvironment": "node"
  }
```

### `2.6. Pruebas unitarias del controlador`

_Mocking:_ La técnica de mocking en un controlador básicamente va a consistir en dar una nueva implementación (el mock) de los servicios que usa, y usar dicha nueva implementación o mock para probar el controlador. Esto lo podemos llevar a cabo de dos formas: mockeando un método concreto del servicio mediante jest.spyOn o mockeando el servicio completo.

### `2.6.1. Mockeo mediante `_*jest.spyOn*_
_jest.spyOn_ nos permite crear una nueva implementación (mock) sobre un método existente de un objeto. Seguiremos este patrón

Ejemplo: _fizzbuzz.controller.spec.ts_

### `2.6.2. Mockeado del servicio completo`

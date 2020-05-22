# DevimFront: tsconfig

Конфигурация Typescript для проектов на TS+React.

## Установка

1. Подключите этот пакет в dev-зависимости.

```bash
npm i -D @devim-front/tsconfig
```

2. Создайте файл `tsconfig.json` в корне проекта со следующим содержимым:

```json
{
  "extends": "@devim-front/tsconfig"
}
```

3. Поскольку TS не умеет разрешать относительные пути из родительской конфигурации, в том же файле `tsconfig.json` следует определить расположение основных каталогов с кодом. Допустим, исходный код проекта хранится в папке `src`, а глобальные типы проекта - в `src/@types`. Тогда `tsconfig.json` должен иметь следующий вид:

```json
{
  "extends": "@devim-front/tsconfig",
  "compilerOptions": {
    "baseUrl": "src",
    "typeRoots": [
      "node_modules/@types",
      "src/@types"
    ]
  },
  "include": [
    "src/**/*"
  ]
}
```

## Полный текст конфигурации

Полный текст конфигурации из библиотеки доступен по ссылке <https://github.com/devim-front/tsconfig/blob/master/tsconfig.json>.
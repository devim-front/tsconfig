# DevimFront: tsconfig

Конфигурация Typescript для проектов на TS+React.

## Установка

1. Подключите этот пакет в dev-зависимости.

```basb
npm i -D @devim-front/tsconfig
```

2. Создайте файл `tsconfig.json` в корне проекта со следующим содержимым:

```json
{
  "extends": "@devim-front/tsconfig"
}
```

## Распространенные примеры кастомизации

Для кастомизациия нужно дописывать правила в файл `tsconfig.json`.

Например, вы хотите __изменить папку, в которой находится исходный код__ c `src` (по умолчанию) на `app`.

```json
{
  "extends": "@devim-front/tsconfig",
  "compilerOptions": {
    "baseUrl": "app",
    "typeRoots": [
      "node_modules/@types",
      "app/@types"
    ]
  },
  "include": [
    "app/**/*"
  ]
}
```

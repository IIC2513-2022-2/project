# ESLint

## ¿Qué es un linter?

Un linter es una herramienta que analiza el código para encontrar problemas o errores tanto de funcionamiento como de estilo. Este análisis se realiza de forma estática, lo que quiere decir que no es necesario ejecutar el código que se está analizando.

## ¿Qué es ESLint?

ESLint es el linter más popular dentro del mundo de JavaScript y es el que usaremos para el proyecto del curso.

## ¿Qué son las reglas de estilo?
Además, de detectar errores o problemas de código, un linter también detecta faltas a un estilo que es definido mediante reglas. Por ejemplo, en JavaScript no es necesario terminar cada línea con un ";", pero es una buena prácitca y algo que un linter podría verificar que se esté haciendo.

## Airbnb
Como el estilo podría considerarse incluso una cosa de gustos, existen múltiples conjuntos de reglas que definen estilos. Para el proyecto aplicaremos un estilo ampliamente usado, el de [Airbnb](https://github.com/airbnb/javascript).

## Instalación
Para poder instalar el motor de ESLint hay que ejecutar el siguiente comando:
```
yarn add eslint --dev
```

Ahora, para configurar las reglas que usaremos:
```
yarn run eslint --init
```

A continuación se muestran preguntas que les aparecerán con las opciones que deben seleccionar para dejar configurado ESLint con las reglas de Airbnb:
- How would you like to use ESLint? **To check syntax, find problems, and enforce code style**
- What type of modules does your project use? **CommonJS (require/exports)**
- Which framework does your project use? **None of these**
- Does your project use TypeScript? **No**
- Where does your code run? **Node**
- How would you like to define a style for your project? **Use a popular style guide**
- Which style guide do you want to follow? **Airbnb: https://github.com/airbnb/javascript**
- What format do you want your config file to be in? **JSON**
- Would you like to install them now? **Yes**
- Which package manager do you want to use? **yarn**

Lo anterior dejará creado el archivo `.eslintrc.json` en el que está la configuración de ESLint y donde además podemos agregar reglas custom o ignorar ciertas reglas.

## Uso de ESLint
Para que ESLint analice código de un archivo en específico o el de todos los archivos que estén en un directorio (y en directorios dentro de ese directorio) corremos el siguiente comando:
```
yarn eslint path/hacia/archivo/o/hacia/directorio
```

En particular si estamos en la raíz de nuestro proyecto y queremos analizar todo el código corremos:
```
yarn eslint .
```

Es importante mencionar que ESLint solo analizará los archivos con extensión `.js`

Hay algunos errores simples que ESLint puede solucionar automáticamente si lo corremos con el flag `--fix`, como por ejemplo:
```
yarn eslint . --fix
```

## Cómo desabilitar una regla
Si hay alguna regla que no les acomoda a su grupo, pueden desabilitarla editando el archivo `.eslintrc.json`. Específicamente en el json asociado a la llave `"rules"` pueden agregar una entrada de la siguiente forma:
```
{
  ...
  "rules": {
    "rule-name": "off"
    }
}
```

Por ejemplo, si queremos que poder tener console.logs en nuestro código sin que sea una falta al estilo podemos poner:
```
{
  ...
  "rules": {
    "no-console": "off"
    }
}
```

## Extensión de ESLint para VSCode
Si están trabajando en VSCode les puede ser de mucha utilidad la extensión llamda ESLint ya que les detectará las faltas que tengan a las reglas que definieron para su proyecto y se las subrayará con una línea roja (similar a cómo Word subraya las faltas a la ortografía). Esto puede ser muy conveniente para evitar tener que estar corriendo eslint desde la consola muy seguido.

Para más información sobre como seguir configurando el linter te invitamos a leer la [documentación de ESLINT](https://eslint.org/docs/latest/user-guide/getting-started).
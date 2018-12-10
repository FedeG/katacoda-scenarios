`let` y `const` son dos formas nuevas de declarar variables que vienen a remplazar a `var`.

## let
Se usa para que las variables solo sean accesibles dentro de un entorno determinado.

## const
Se usa para variables que ademas de ser accesibles dentro de un entorno determinado son de solo lectura.

## Ejemplos
Vamos a usar el archivo `variables.js`: `variables.js`{{open}}

En el archivo vamos a ver un `if` con un bloque de codigo en donde se crean dos variables (`x` e `y`) y cada una de distinta manera.

Si desde de esa variable agregamos:
<pre class="file" data-filename="variables.js" data-target="append">console.log(x);
</pre>

Ejecutamos el codigo: `node variables.js`{{execute}}

Como usamos `var` en la declaración de la variable, `x` sigue existiendo

Pero si agregamos:
<pre class="file" data-filename="variables.js" data-target="append">console.log(y);
</pre>

Ejecutamos el codigo: `node variables.js`{{execute}}

Como usamos `let` en la declaración de la variable, no existe en esta parte del codigo, solo existe dentro del bloque del if

Dentro del mismo archivo podemos ver otas dos variables (`a` y `b`) que también estan declaradas cada una con un tipo.

Si agregamos:
<pre class="file" data-filename="variables.js" data-target="append">
b = 'otro valor';
console.log(b);
</pre>

Comentamos los `console.log` anteriores y ejecutamos el codigo: `node variables.js`{{execute}}

Como la variable `b` esta definida con `let`, podemos modificarle el valor

Pero si agregamos:
<pre class="file" data-filename="variables.js" data-target="append">
a = 'otro valor';
console.log(a);
</pre>

Ejecutamos el codigo: `node variables.js`{{execute}}

Como la variable `a` esta definida con `const`, al querer cambiarle el valor a la constante vamos a ver un error: `'TypeError: Assignment to constant variable.'` y el valor de `a` va a seguir siendo `'var'`
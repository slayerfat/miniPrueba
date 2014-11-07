miniPrueba
==========

Repositorio en donde se manejara el codigo referente al sistema.


# en construccion!

### este repositorio estara referido por todos los integrantes del grupo. la idea es que se familiarizen (a los que le de la gana) para que trabajen en esto.

en muy poco tiempo me di cuenta que git es elemental y todos deben usarlo, simplemente por control, y validacion de codigo, como uds. estaban trabajando era una locura, eso tiene que cambiar.

ok, lo elemental para empezar a usar el git:

bajar el git desde la pagina web de github.

o por linux:

```
sudo apt-get update
```
para que se actualice la informacion de linux y sus archivos.

```
sudo apt-get install git
```
para instalar git como tal

## GIT no es GITHUB

github es un servicio tipo facebook.

git es gnu hecho por el mismo que hizo linux (linus torvalds)
aprendan: [Linus T](en.wikipedia.org/wiki/Linus_Torvalds)

luego de esto

chequean que todo este bien:

```
git --version
```
si todo esta bien saldra algo como:
```
git version 1.9.1
```

si no sale eso, algo esta mal, reinicia la pc e intenta de nuevo.

## OK ya tienes git en tu sistema, ahora que???

BUENO! MIRA!

crea una carpeta donde te de la gana en tu sistema:

```
mkdir carpetaTal
```
o como te de la gana de crearla. yo la cree como 

```
mkdir github
```

luego tienes que ir a esa carpeta `cd carpetatal`

OK MIRA LO DIFICIL QUE ES ESTO:

configuras el asunto localmente:

correo:

```
git config --global user.email "slayerfat@gmail.com"
```
seudonimo:
git config --global user.name "slayerfat"

esto **no es para github**, esto es para tener esos datos localmente, ya que por cosas que tienen que hacer mas adelante, es excelente cuando ya tienen esto configurado.

###OK YA SALIMOS DE LA PARTE MAS DIFICIL!!!

#GIT CLONE


(asegurate de estar en la carpeta que hayas creado anteriormente, 
en mi caso fue **github**)


##y ahora?

bueno man:

```
git clone direcionDelRepositorio
```

eso es todo, asi tienes una copia completa y actualizada de los archivos, **que dificil verdad??**

ejemplo para clonar este repositorio:

```
git clone https://github.com/slayerfat/miniPrueba
```

_CUIDADO BILL GATES! TE TUMBO EL NEGOCIO!_

ok ahi acabas de clonar el repositorio localmente en tu sistema:
	(_suponiendo que creaste un directorio llamado github:_)

```
ls github
```

deberias ver una carpeta nueva llamada
**sistemaJag**

dentro de esta carpeta estara exactamente lo mismo que hay en este repositorio.

###YUPPIIIIII

aja y entonces???

bueno mira:

#GIT STATUS

si quieres saber en que forma se encuentra tu clon en relacion al repositorio central:
```
git status
```

esto lo que hace literalmente es chequear el estatus del repositorio en relacion a lo que acabas de clonar.

existen muchas razones por las que tienes que hacer `git status` entre ellas esta la idea de que sepas como esta la sincronizacion entre tu y el repo.

##el repositorio:

el repositorio principal se llama master, considera master como la matriz principal en donde todos trabajamos.

* master
	* tu clon local

tu clon local es subdito de master, si master cambia, tu cambias, si tu cambias, cambias a master.

por ejemplo si cambiaste un archivo saldra algo como:

```
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   README.md

```

ahi se lee venezolanamente:

```
cambiastes vainas:
	usa los comandos tal si quieres:

	modificado: README.md
```

#GIT ADD

##OK EMPIEZAS A CAMBIAR DATOS DENTRO DE LOS archivos

agarro index... agarro este formulario... hago esto otro...
ajusto una variable... cambio este javascript... modifico esta condicion...
cambio la base de datos....
la vuelvo a CAMBIAR....
reajusto la base de datos....
me quejo sobre la base de datos...
MALDITA BASE DE DATOS!!!!!!!QAGQ#!!!M#L!G#

... la base de datos.

ok, luego que hayas hecho tus modificaciones:

##PREPARA TU MENTE PORQUE NO RESPONDO:

primero haces un `git status` para que veas todos los archivos que tienen cambios en relacion con el repositorio(master).

automaticamente vas a ver archivos que tu cambiaste y archivos que otros cambiaron de master desde otro lugar en otro momento.

chevere... ahora haces un

```
git add -A
```
-A significa todos los cambios que hiciste, sino lo tienes que hacer manualmente:

```
git add archivoTal.php
```

```
git add otroArchivo.js
```
etc.

CON MUCHA PRECAUCION chequeamos que lo que hicimos esta bien.



y si haces un chequeo adicional (`git status`) veras que ahora los archivos estan listos para ser mandados, este proceso se llama commit.

por ejemplo, el resultado cuando haces add de los archivos y haces un git status es:

```
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   README.md

```

```
en venezolano:

cambios a ser mandados:
	usa tal comando si te da la gana:

			modificado: archivoTal.tal
```

#GIT COMMIT

lo mas dificil del mundo, mandar los archivos al repositorio para que se sincronicen y demas, esto se hace con una simple linea de codigo:

```
git commit -m "tus comentarios sobre los cambios que decidiste hacer"
```

git se encarga automaticamente de sincronizar todo, desde tu clon a master y viceversa.

##es importante:

este es un buen momento para hacer enfasis sobre el hecho de documentar tus cambios.

trata de ser descriptivo, habla sobre los cambios y porque los hiciste.

acuerdate que el equipo no necesariamente sabe lo que tu hiciste, y tu esperar que el equipo te diga lo que han hecho.

todo esto es para perder el menor tiempo posible, porque ha pasado que tengo que llamar o me llaman preguntando sobre algo del codigo o cambios que se hicieron, etc, por no estar documentado.

se hace un ultimo `git status` para ver que todo esta bien, deberia decir algo como up to date, que dice en español algo como actualizado.

**y ya, eso es todo lo basico...**

y este proceso se repite una y otra vez en cada momento que hagas cambios importantes.

piensa en el git commit como  datos que PLANEAS MANDAR, no como datos que ya enviaste o estas enviando.

#GIT PUSH

piensa en el push como datos que ESTAS MANDANDO concretamente.

simplemente haces un 

```
git push
```

y ya, mandaste los cambios al repositorio (en este caso github)

como es una conexion https encriptada te pedira tu usuario y contraseña:

```

Username for 'https://github.com': tuSeudonimo
Password for 'https://slayerfat@github.com': <i>tu clave</i>

```

listo papa, ya hiciste un cambio a master.


en resumen, sin tanta paja:

#resumen

clonamos:

```
git clone https://github.com/slayerfat/miniPrueba
```

chequeamos el estatus:

```
git status
```

(haces cambios a los archivos)

chequeamos el estatus otra vez:

```
git status
```

decidimos preparar los archivos a ser mandados al repositorio(master)

```
git add -A
```
para asegurarnos:

```
git status
```

y por ultimo:

```
git commit -m "tus comentarios SOBRE TU IMPORTANTE CAMBIO!! (se descriptivo) "
```
```
git status
```

y por ultimo haces el push a master:

```
git push
```


ESO ES TODO.

luego hablar sobre como hacer otras cosas. esto es lo mas basico.
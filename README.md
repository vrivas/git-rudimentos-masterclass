# git-rudimentos-masterclass
Rudimentos de git para explicar en una Masterclass al efecto

## Qué es Git
GIT es un sistema de control de versiones.

Sirve para llevar un registro de modificaciones en ficheros: 

* QUÉ se ha hecho
* CUÁNDO se ha hecho
* QUIÉN lo ha hecho

## Qué NO es Git

* No es un sistema para tener copias de seguridad en la nube... 

(Pero funciona realmente bien como sistema de copias de seguridad en la nube).
* No es un sistema especialmente indicando para trabajar con otro tipo de ficheros que no sean ficheros de texto.

(Pero funciona realmente bien con otros tipos de ficheros además de lo de texto).
  

## De directorio a repositorio
```
git init
```

## Estado de mi repositorio
```
git status
```

## Seguir la pista a un fichero
```
git add nombre_fichero
```

## Confirmar que queremos registrar los cambios realizados en un fichero
¡¡No olvides grabar primero los cambios hechos en tu fichero!!

```
git commit -m "Mensaje"
```
## ¿Problemas de autoría?
```
git config user.name "Ataulfo Rodendrales Mirapuertas"
git config user.email "arodendrales@ujaen.es"




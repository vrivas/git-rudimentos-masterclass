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
  
## Repos locales
### De directorio a repositorio
```
git init
```

### Estado de mi repositorio
```
git status
```

### Seguir la pista a un fichero
```
git add nombre_fichero
```

### Confirmar que queremos registrar los cambios realizados en un fichero
¡¡No olvides grabar primero los cambios hechos en tu fichero!!

```
git commit -m "Mensaje"
```
### ¿Problemas de autoría?
```
git config user.name "Ataulfo Rodendrales Mirapuertas"
git config user.email "arodendrales@ujaen.es"
```
### Flujo básico de trabajo
**¡Ojo al paso 3!**

1. Creo/edito un fichero.
2. Guardo el fichero
3. `git add nombre_del_fichero`
4. `git commit -m "Breve mensaje explicativo"`

### Abreviando un poco
Si tenemos la certeza de que todos los cambios hechos en los distintos ficheros se corresponden con una única tarea, podemos ahorrarnos el `git add` de los ficheros que habían sido ya añadidos antes:

1. Edito un fichero que ya formaba parte del repo.
2. Guardo el fichero
3. `git commit -a -m "Breve mensaje explicativo"`

**¡¡OJITO CON LOS 'y' EN LOS MENSAJES EXPLICATIVOS!!**

### Historial de cambios
```
git log
```

### Un pelín de interfaz *"""""""más humana"""""""*
```
git instaweb
git instaweb --stop
```






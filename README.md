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

### Vayámonos por las ramas
```
git branch           # Listar ramas
git branch nueva     # Crear nueva rama 'nueva'
git switch nueva     # Cambiar a la rama 'nueva'
git checkout nueva   # Equivalente a switch
git switch -c otra_mas # Equivalente a branch+switch
...
...
git switch main      # Cambiar a la rama 'main'
git merge nueva      # Incorpora los cambios que haya en la rama 'nueva' a la rama 'main'
```
## Los commits pueden ser puntos de partida de nuevas ramas
```
git log                # Para ver los commits
git checkout c03fcb    # Para cambiar al estado que refleja dicho commit
git switch -c rama_desde_commit # Para crear la rama desde ese punto
```

## Los commits pueden permitirnos empezar desde un determinado punto
```
git log
git reset --hard e3d24c  #¡¡OJO¡¡ PERDEMOS TODO EL TRABAJO POSTERIOR A ESE COMMIT
```

## Repos remotos
### Crea el repo
**¡¡Empieza mejor en el sitio web del gestor de Repos!!**

1. Ve a GitHub y date de alta.
2. Crea un repo.
3. **CLONA** el repo. ¿Necesitas clave pública?
4. Trabaja en tu repo local: editar > grabar > ¿git add? > git commit
5. **SINCRONIZA** el repo remoto: `git push`

### Tu workflow diario
1. **SINCRONIZA** el repo local: `git pull`
2. Trabaja en tu repo local: editar > grabar > ¿git add? > git commit
3. **SINCRONIZA** el repo remoto: `git push`

* `git pull` una vez. 
* `git push`siempre que quieras. 
* Puedes incluir más de un commit.

### Publica ramas locales
```
git switch -c rama_nueva                      # Crea la rama local
git push --set-upstream origin rama_prueba    # Crea la rama remota y las asocia
```

### Borra ramas
```
git branch -d rama_prueba                    # Borra la local
git branch -d --remote origin/rama_prueba    # Borra la remota
```


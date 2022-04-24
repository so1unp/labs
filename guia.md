---
lang: es-ES
---

# Guía Laboratorios SO

Como trabajar con Git

## Repositorios

Los alumnos generan su repositorio mediante un _link_ generado desde [GitHub Classroom](https://classroom.github.com/). De esta manera cada alumno cuenta con un repositorio *privado* por cada laboratorio, dentro de la organización [so1unp](https://github.com/so1unp). A este repositorio sólo tienen acceso el alumno y la cátedra.

Una vez generado el repositorio, los alumnos pueden clonar el mismo en su cuenta en el servidor de la cátedra o en sus PCs:
```
$ git clone https://github.com/so1unp/lab01-nombrealumno
```

## Workflow con Git y GitHub

### Simple

El alumno genera _commits_ en la rama `master` mientras avanza con el desarrollo del laboratorio. 

Ejemplo: 
```
$ vi ejercicio1.c
$ git add ejercicio1.c
$ git commit -m "Ejercicio 1 resuelto"
$ git push
```

El alumno edita el archivo `ejercicio1.c` y realiza el _commit_ de la modificación. Suponiendo que considera que el ejercicio esta resuelto, _sincroniza_ el repositorio subiendo estas modificaciones en el repositorio _remoto_ en GitHub mediante el comando `git push`.

### Avanzado

El alumno debe generar una rama para cada ejercicio. Cuando considera que el ejercicio esta finalizado genera un _pull request_ desde la web de GitHub. La cátedra entonces revisa la solución del ejercicio. Si se considera que se debe modificar algo o se encuentra un error, se generan los comentarios e indicaciones en el _pull request_. El alumno puede seguir realizando modificaciones en la rama y estos _commits_ son automáticamente integrados en el _pull request_. Una vez se considera que el ejercicio esta resuelto satisfactoriamente la cátedra realiza el _merge_ de la rama del ejercicio con la rama principal del repositorio.

#### Ejemplo:
```
$ git checkout -b ej1
$ vi ejercicio1.c
$ git add ejercicio1.c
$ git commit -m "Ejercicio 1 resuelto"
$ git push origin ej1
$ git checkout master
```

Antes de iniciar el ejercicio, el alumno crea la rama _ej1_ desde la rama _master_. Cuando considera que el ejercicio esta finalizado, sincroniza los cambios en el repositorio remoto mediante el `git push`. Luego, desde la web de GitHub, genera el _pull request_.

### Alternativo

Se pueden generar archivos .zip de los repositorios y distribuirlos a los alumnos. Estos pueden luego enviar los laboratorios resueltos de la misma manera.

## Servidor remoto

El servidor ya tiene todo el software necesario para realizar los laboratorios.


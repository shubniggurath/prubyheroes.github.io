---
layout: post
title:  Cómo empezar un proyecto con Jefe?
date:   2017-07-17
categories: setup
---

# Qué es `jefe`?
`jefe` es wrapper para docker realizado por Daniel Gamboa Estrada, este nos da algunas tareas que facilitan la creación y manejo
de docker y docker-compose.

Este lo podemos encontrar en este [repositorio](https://github.com/dgamboaestrada/jefe)

Al instalar este script en el host podremos ocupar el comando `jefe` que nos permite crear un scaffold de proyectos como `wordpress`, `cakePHP`,
`Symfony`, `Laravel` y `Ruby on Rails`. Esto nos ahorra el trabajo de empezar la base de un proyecto para cualquiera de estos frameworks con la ventaja
de usar un entorno de virtualización sobre Docker usando Docker Compose.

El uso de `jefe` como base representa el pilar del flujo de desarrollo y el uso de otras herramientas ya que permite estandarizar el ambiente de desarrollo
local para un equipo de desarrollo.

# Empezando un proyecto con `jefe`

## Instalando `jefe`
Para instalar jefe solo hay que seguir las instrucciones que se encuentran en el README del repositorio oficial,
al día de hoy son las siguientes.

```
curl -O https://raw.githubusercontent.com/dgamboaestrada/jefe/master/jefe-cli.sh
chmod +x jefe-cli.sh
sudo mv jefe-cli.sh /usr/local/bin/jefe
```
Una vez completada esta acción debemos checar la instalación con el siguiente comando
```
jefe version
```
Este comando nos debe devolver una salida como la siguiente.

```
0.2
```
Esta es la versión al día en que se hace esta guía, si esta no fue la salida por favor reviza tu instalación.

## Haciendo un scaffold
Como ya lo mencionamos `jefe` tiene capacidad para crear scaffold para varios tipos de frameworks en este caso iniciaremos uno
con Ruby on Rails.

Debemos estar seguros que `jefe` esta instalado.

Una vez hecho esto procedemos a crear una carpeta la cuál contendrá nuestro proyecto.

```
mkdir test_project_rails
cd test_project_rails
```

Una vez hecho esto procedemos a correr el comando `jefe init` para empezar el scaffold del proyecto.
```
# /test_project_rails
jefe init
```
`jefe` desplegará un menu en el cual podremos elegir la opcion de Ruby para crear nuestro proyecto con Ruby on Rails

![jefe init]({{ site.url }}/uploads/2017/07/Screenshot_20170817_173023.png)

`jefe` pedira un nombre para el proyecto en este caso pondremos test_project_rails, el valor por default es `docker_ruby`.



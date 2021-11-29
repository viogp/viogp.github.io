---
layout: post
title: Obsidian con Github en dispositivos móviles
tags: [notas, git]
---

Recientemente me he puesto a aprender sobre la gestión del conocimiento personal, con el curso de [Guía Carmona](https://unbuenplan.blog/author/guiacarmona/), [Nota a Nota](https://unbuenplan.blog/2021/11/02/por-que-instalarte-una-nueva-aplicacion-de-notas-no-va-a-solucionar-tus-problemas-con-la-gestion-del-conocimiento/). La idea básica es tener un sistema funcional para capturar ideas, ordenarlas, procesar la información y expresarla a tu manera.  

A raíz de este curso, he descubierto de la existencia de [org-mode](https://www.orgmode.org/index.html) y [org-roam](https://www.orgroam.com/manual.html) de [emacs](https://www.gnu.org/software/emacs/), pero he visto que, por el momento, es un tanto complicado utilizarlos con el móvil y el iPad para capturar información. Así que he decidido probar [Obsidian](https://obsidian.md/) en mis dispositivos móviles para empezar a aplicar lo que voy aprendiendo sobre gestión de conocimiento.

[Obsidian](https://obsidian.md/) es un sistema de notas  local, con la posibilidad de enlazarlas. Así que la única dificultad para configurar esta aplicación es la sincronización de las notas entre dispositivos. Hay varias opciones, y yo he decidido utilizar un repositorio en  [GitHub](https://github.com/).

## Repositorio en [GitHub](https://github.com/)
En [GitHub](https://github.com/) he generado un repositorio nuevo, que vamos a llamar `mirepo.git`.

## Obsidian en el iPad
1. Instalar las applicaciones de [Obsidian](https://obsidian.md/) y [Working Copy](https://workingcopy.app).
2. Clona tu repositorio en [Working Copy](https://workingcopy.app)
3. En [Obsidian](https://obsidian.md/), genera una  *bóveda* (*vault*) nueva que **no** esté sincronizada con iCloud.
3. En  [Working Copy](https://workingcopy.app) configura un repositorio para poder compartirlo con [Obsidian](https://obsidian.md/): *Setup Folder Sync* -> *On My iPad, Obsidian*.

## Obsidian en un móvil con Android
1.  Instalar las applicaciones de [Obsidian](https://obsidian.md/) y [Termux](https://termux.com/).
2.  Dentro de [Termux](https://termux.com/), [generar llaves SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent). Si quieres guardar tus llaves SSH con el nombre *misllaves*: `$ ssh-keygen -t rsa -b 4096 -f ~/.ssh/misllaves`.
3. [Añadir la llave SSH pública](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) (por ejemplo, lo que hay dentro de *misllaves.pub* en el directorio `~/.ssh` del paso anterior) a tu perfil en  [GitHub](https://github.com/).
4.  En [Termux](https://termux.com/), genera un directorio de almacenamiento, `/storage/shared`, ejecutando el siguiente comando: `$ termux-setup-storage`. 
5. En [Termux](https://termux.com/), vete al directorio de almacenamiento: `$ cd storage/shared`. 
6. En el directorio de almacenamiento compartido que has creado en [Termux](https://termux.com/), clona tu repositorio: `$ git clone git@github.com:[nombre de tu usuario en GitHub]/mirepo.git`
7.  Abre  [Obsidian](https://obsidian.md/) en tu móvil de Android y abre una *bóveda* (*vault*) desde la carpeta con el repositorio que acabas de clonar.

## Utilizando Obsidian en tus dispositivos móviles
Para utilizar [Obsidian](https://obsidian.md/) en tus dispositivos móviles con [GitHub](https://github.com/), recuerda actualizar tus notas antes de ponerte a escribir:
*  En [Working Copy](https://workingcopy.app) o en  [Termux](https://termux.com/) (desde el directorio con tu repositorio): `$ git pull`.

Y al terminar, actualiza tu repositorio en  [GitHub](https://github.com/):
*  En [Working Copy](https://workingcopy.app) o en  [Termux](https://termux.com/) (desde el directorio con tu repositorio): 
	1. Añade tus ficheros nuevos: `$ git add mificheronuevo`.
	2. Comprueba el estado del repositorio: `$ git status`.
	3. Guarda localmente tus cambios: `$ git commit -am "he añadido un nuevo fichero"`.
	4. Actualiza  tu repositorio en  [GitHub](https://github.com/): `$ git push`.

---
Páginas de las que he sacado información para desarrollar mi configuración:

* [Obsidian en el iPad enlazado a GitHub a través de Working Copy](https://ryan.himmelwright.net/post/obsidian-ios-setup/).
* [Obsidian en Android via termux](https://www.greghilston.com/post/how-i-use-obsidian-mobile-with-git-on-android/).


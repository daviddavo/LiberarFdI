# Fundamentos de Computadores

## Eclipse para ARM

### 1. Descripción del programa
Eclipse es un Entorno de Desarrollo Integrado (IDE), como Visual Studio, pero libre y multiplataforma.

Para la asignatura de 1º de Fundamentos de Computadores
vamos a emular código ensamblador de ARM usando este entorno.

Existen distintas versiones de Eclipse, algunas con algunos paquetes preinstalados para un lenguage determinado. Si quieres programar en C/C++ te descargas Eclipse C/C++ y si quieres programar en Java te descargas eclipse para Java.

El problema es que, para programar en ARM no tienes un "Eclipse ARM". En su lugar tienes diversos plugins que añaden funcionalidades al Entorno, para poder, por ejemplo, emular código ensamblador.

### 2. Requisitos de Hardware

- Un ordenador
- Un teclado (recomendado)
- Un ratón (opcional)

Depende mucho de lo que quieres que tarden en compilar tus programas. En general, consume menos recursos que Visual Studio, por lo que, si te funciona Visual, te funcionará Eclipse.

### 3. Guía de instalación

#### Windows
En el Campus Virtual encontrarás un .exe instalador que lo único que hace es
1. "Instalar" eclipse C/C++
2. "Instalar" un compilador de ARM
3. "Instalar" varios plugins para trabajar con ARM (Debugger, simulador, etc)

En realidad lo que hace es descomprimir una versión portable (de hace 5 años, por cierto) en donde le indiques.

Esto lo podemos hacer perfectamente "a mano" en cualquier otra máquina, pues tanto Eclipse como sus plugins son software libre y están disponibles para cualquier plataforma. Es lo que vamos a hacer a continuación para instalarlo en Linux

#### GNU/Linux
Para los ejemplos durante la instalación usaremos Arch Linux y Ubuntu

Lo primero de todo, vamos a instalar eclipse, la versión de C/C++ nos vendrá perfectamente

`pacman -S eclipse-cpp`

También vamos a necesitar un compilador, en clase usamos arm-none-eabi-gcc, que instalaremos con
`pacman -S arm-none-eabi-gcc arm-none-eabi-binutils arm-none-eabi-gdb arm-none-eabi-newlib`

Ahora nos falta instalar el emulador
`pacman -S qemu-arch-extra`

Una vez instalado todo, vamos a abrirlo. Cuando lo abras te dirá que le indiques un espacio de trabajo (Workspace). Aquí se van a guardar tus proyectos (si no le indicas otra ruta) y otras configuraciones. Para no tener que indicarle cada vez que lo abres dónde está el Workspace, activa la casilla para que no te pregunte de nuevo.

![Fig 1. Select a Workspace](https://i.imgur.com/yhrtJhh.png)

En Eclipse vamos a instalar el plugin GNU MCU Eclipse, que contiene varias herramientas para trabajar con ARM.
(Nota. Hacer captura de como instalar un plugin)

Seguimos con las instrucciones indicadas en la práctica, pero en el paso 8, en lugar de hacer click en ARM Sourcery GCC C Linker->General, haremos click en GNU ARM Cross C Linker -> General

### 4. Anexos

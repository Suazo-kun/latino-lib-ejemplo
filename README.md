# latino-lib-ejemplo
Ejemplo minimo para crear una libreria para [latino](https://github.com/lenguaje-latino/latino) en C.
En el archivo src/latino-libejemplo.c se encuentra comentado con lo minimo que se requiere.

## Instalación

### Linux

#### Prerequisitos

Ejecutar lo siguiente en la terminal según tu distribución:<br>
##### Debian/Ubuntu:
```Bash
sudo apt update
sudo apt install build-essential cmake libreadline-dev git
```

##### Fedora:
```Bash
sudo dnf check-update
sudo dnf groupinstall "C Development Tools and Libraries" "Development Tools"
sudo dnf install cmake readline-devel git
```

##### Arch:
```Bash
sudo pacman -Sy
sudo pacman -S base-devel cmake readline git
```

Y para compilar la librería ejecutar lo siguiente en la terminal:

```Bash
git clone https://github.com/Suazo-kun/latino-lib-ejemplo
cd latino-lib-ejemplo
mkdir build
cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
sudo make install
```

### Termux

#### Prerequisitos

Ejecutar lo siguiente en la terminal:
```Bash
pkg update
pkg install build-essential cmake libreadline-dev git
```

Y para compilar la librería ejecutar lo siguiente en la terminal:

```Bash
git clone https://github.com/Suazo-kun/latino-lib-ejemplo
cd latino-lib-ejemplo
mkdir build
cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make install
```

### Windows

#### Prerequisitos

Tener instalado:
[latino](https://github.com/lenguaje-latino/latino)
[cmake](https://cmake.org/download/)
[visual studio](https://visualstudio.microsoft.com/es/vs/community/)

Ejecutar lo siguiente en cmd:

```
git clone https://github.com/Suazo-kun/latino-lib-ejemplo
cd latino-lib-ejemplo
mkdir build
cd build
cmake -G "Visual Studio 16 2019" -DCMAKE_BUILD_TYPE=Release ..\
```

Abrir con visual studio 2019 y compilar la solucion latino-lib-ejemplo.sln 
generada en la carpeta build/

Compilar el proyecto en modo Release.

Para instalar la libreria abrir visual studio con permisos de administrador
Generar el proyecto de INSTALL.vcxproj dando clic derecho sobre el proyecto y build
o copiar la libreria .dll generada con este proyecto en la ruta de instalación
de latino. 
Por ejemplo:

`C:/Program Files/Latino/bin`

### MSYS

Abrir una terminal de MSYS y correr lo siguiente.

```Bash
pacman -Sy
pacman -S libreadline libreadline-devel
git clone https://github.com/Suazo-kun/latino-lib-ejemplo
cd latino-lib-ejemplo
mkdir build
cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make install
```

## Uso de esta librería en código latino

```
// incluye el modulo en latino
incluir("libejemplo")

x = libejemplo.suma(1, 1.5)

escribir(x)
```

ver ejemplo.lat

### Ejecutar el ejemplo:
`latino ejemplo.lat`


### Dependecias

Ninguna

#### Cualquier aportación o sugerencia es bienvenida

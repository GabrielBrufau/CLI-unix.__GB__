# TERMINAL.__GB__
```bash
/ - etc
  - dev
  - home {
          jono {
                work
                photos
                }
          mako
          cory 
         }
  - usr  {
          lib
          }
  - var
```
# visual studio
```bash
code .nombredelarchivo //? abre el archivo en visual
```
# comandos
```bash
ls //? muestra las carpetas de donde estamos ubicados
ls -l //? muestra los archivos 
ls -lh //? le da una lectura mas humana
ls -la //? muestra todos los archivos incluido los archivos ocultos
ls -lS //? muestra y ordena por tamanios
ls -lr //? muestra los archivos de la z a la a re reverse
ls *.txt //? busca todos los archivos que terminan en txt
ls primeraspalabrasdelarchivo* //? busca todos los archivos que conincidan con las palabras que pongas antes del *
ls primerasletrasdelarchivo? //? busca todas las coincidencias que tengan las letras y solo un caracter final
ls primerasletrasdelarchivo??? //? busca todas las coincidencias que tengan las letras y solo tres caracter final
ls [[:upper:]]* //? busca todas las carpetas que empiezan con uppercat mayusculas
ls -d [[:upper:]]* //? busca todas los directorios que empiezan con uppercat mayusculas
ls [[:lower:]]* //? busca todas las carpetas que empiezan con minusculas
ls nombrefile > nombrefile //? copia/sobrescribe lo que hay en el primero al segundo
ls nombrefile >> nombrefile //? concatena los archivos con el nuevo nombre que le des si no existe lo crea
ls archivoquedaunerror 2> error.txt //? crea un archivo que dentro podemos visualizar el errror con el comando head
ls archivoquenosavemoscomoresultara > output.txt 2>&1 //? si no sabemos si el archivo nos va a arrojar un arror o reject
ln -s rutade/ejemplo linkdeejemplo //? acceso directo
less nombredelarchivo //? te muestra todo el archivo {
                                                      /nombredelabusqueda //?permitebuscar una palabra
                                                      q //?para salir
                                                      }
cd //? cd sin parametros te lleva a home
cd nombredelarchivoocarpeta//?entra a el archivo o carpeta
cd .. //? de lleva una carpeta mas atras
clear //? borra la vista dela terminal
pwd //? muestra la ruta de donde estamos
file //? da mucha informacion
find ./ <name nombredelarchivo //? busca todos los archivos que se llamen asi
find ./ -name *.txt | less //? busca todos los archivos que terminen en eso y te da info
find ./ -type f -name nombredelfile //? busca por type
find ./ -type d -name nombredeldirectorio
find ./ -type f -name *.log //? busca el archivo .log
find ./ -size 20M //? busca los archivos por taman:o mayores a 20 megas
mkdir dir1 dir2 etc//? crea un directorio
touch file1 file2 //? crea un archivo
> nombredelarchivo.txt //? crea un archivo de texto
cp filenametocopy newfilenametoname //? copia el archivo

mv filenametomove ..(rutatomove) //? nos permite mover un archivo
mv filename newfilename //? renombra el archivo
rm filename //? remueve el archivo
rm -i filename //? interactivo
rm -rf //? fuerza remover cualquier archivo
rm -ri dir1 //? va a borrar de a un archivo hasta el dir1 preguntandote
rm -r dirname dirmane dirname //? remueve los directorios
head nombredelfile //? muestra el contenido del archivo primeras 10 lineas
head nombredelfile -n 15//? modifica las primeras lineas que tira por defecto ahora son 15
tail nombredelarchivo //? nos muestra las ultimas lineas de un archivo
tail nombredelfile -n 15 //? las ultimas 15 lineas

xdg-open nombredelarchivo //? te abre el archivo con el editor de texto predeterminado
nautilus nombredelarchivo //? abre el archivo con otra iunterfas grafica
help cd(alguncomando) //?nos muestra todo lo que podemos hacer con ese comando
man cd(alguncomando) //? nos muestra todo lo que podemos hacer con ese comando
info cd(alguncomando) //? nos muestra todo lo que podemos hacer con ese comando
whatis cd(alguncomando) //? nos muestra  que podemos hacer con ese comando
echo "hola mundo" //? solo genera una salida en la terminal
echo $nombredelavariabledeentorno //? imprime la variable de entorno
cat unarchivo segundoarchivo //? concatena archivos
cat nombredelarchivo //? lee el archivo
cat > nombredelarchivo //? permite escribir dentro del archivo Ctrl d para dejar de escribir
chmod numerosenmodooctal nombredelarchivo //? cambia los permisos del archivo
chmod u-r nombredelarchivo //? la u es de usuario el menos de de quitar la r es de lectura
chmod u+r nombredelarchivo //? le da los permisos de lectura
chmod u-x,go=w nombredelarchivo //? esto le da al usuario un permiso de ejecucion,go, al grupo como a otros le da un permiso de write
whoami //? le pregunta ala maquina quienes somos
which nombredelprograma //? busca la ubicacion del programa
id //? nos da informacion del usuario extra
su nombredeusuario //? cambiamos de usuario
su root //? nos cambiamos al mitico user root 
sudo //? te da los permisos del user root podras borrar archivos root desde cualquier user
passwd //? nos permite cambiar la contrasenia de cualquier user
grep //? es un comando que permite filtrar alguna palabra que busques en determinado archivo
```
# tipos de archivos
```bash
- //?un archivo normal
d //?un directirio
l //? un link simbolico
b //?un archivo de bloque especial son los archivos que manejan la informacion de los bloques de datos como una USB
```
# tipos de modo
```bash
duen:o  rwx 111
grupo  r-x  101
word  r-x  101
```
# modo octal
```bash
octal   binario   permisos
0       000       ---
1       001       --x
2       010       -w-
3       011       -wx
4       100       r--
5       101       r-x
6       110       rw-
7       111       rwx
```
# tipos de permisos
```bash
r //? permisos de lectura
x //? permisos de ejecucion
w //? permisos de escritura

```
# modo simbolico
```bash
simbolo       significado
u             solo para usuarios
g             solo para el grupo
o             solo para otros(es el word)
a             Aplica para todos
```
# 4 types of comandos 
```bash
type nombredelcomando //? nos muestra el typo de ese comando
```
Un programa ejecutable
```bash

```
Un comando de utilidad de la shell
```bash

```
Una funcion de shell
```bash

```
Un alias
```bash
alias l="ls -lh" //? crea un nuevo comando que remplasa lo que hacia ls -lh
```
## funciones con comandos
```bash
ls; mkdir holi; cal //? el punto y coma nnos permite correr multiples comandos
ls & date & cal //? permite ejecutar varios comandos de forma asincrona
mkdir test && cd test //? crea la carpeta test y si la crea entra a esta
cd archivoquenoexiste || touch archivo.txt && echo "si funca"//? no le importa si algun procesi falla continua con el otro
```
# modificar los permisos en la terminal
```bash
chmod 755 nombredelarchivo //? cambia los permisos del archivo

```
# variables de entornos
```bash
printenv //? nos muestra todas las varialbles de entornos que tenemos configuradas
//para modificar las variablkes de entorno
ls -la buscamos bashrc //? miramos como si se encuentra ese erchivo
code .bashrc //? lo abrimos con visual estudio

```
# utilidades de red
```bash
ifconfig //? muestra enformacion de red direcciones puertos sertvidores
ping www.google.com //? da informacion de la conectividad de una pagina
curl www.google.com //? trae el codigo de la pagina
curl www.google.com //? > index.html
wget www.google.com //? descarga el archivo a la computadora
traceroute www.google.com//? todas las computadoras que intervienen que intervienen en el camino para llegar a google
netstat -i //? muestra los dispocitivos de red

```
# comprimiendo archivos 
```bash
tar -cvf archivoacomprimir.tar nombredeldirectorio //? tar comprime archivos -c (comprimir) v(muestra el ouput en la terminal) f (porque va a comprimir un file)
tar -cvzf archivoacomprimir.tar.gz nombredeldirectorio //? tar comprime archivos -c (comprimir) v(muestra el ouput en la terminal) f (porque va a comprimir un file) z (le comprime en archivo.zip)
tar -xzvf archivoadescomprimir.tar.gz
zip -r archivoacomprimir.zip nombredeldirectorio //? comprime el archivo en zip
unzip archivoadescomprimir.zip 
```
# manejo de procesos
```bash
ps //? muestra los procesos que estan corriendo en nuestra terminal actualmente
top //? muestra los procesos que estan usando mas recursos
kill //? mata procesos desde nuestra terminal
```
# vim
```bash
vim //? para entrar a vim
:q //? para salir de vim
vim index.html //? crea un archivo index en el aditor
```
# personalizacion de la terminal


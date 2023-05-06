# Hello World!

Bienvenido a tu primer programa en Go.

Como es de costumbre a la hora de aprender un lenguaje de programación, empezaremos por nuestro primer hello worlld!

1. Dentro de tu /home creamos un directorio donde almacenar nuestro código:
```
mkdir go-programs
```
2. Dentro de nuestro nuevo directorio creamos un fichero llamado hello.go:
```
touch hello.go
```
3. Con tu editor favorito copiamos el siguiente código y guardamos:
```
package main
import "fmt"
func main() {
    fmt.Println("hello world")
}
```

4. Ahora tenemos dos opciones disponibles en Golang:
#### go run
> Golang tiene dos comandos disponibles que se comportan de manera similar:
>
```
go run
```
>
> Ejecutamos en nuestra terminal el siguiente comando:
```
go run hello.go
```
> Resultado en pantalla
```
Hello world!
```
> Si miras dentro del directorio, verás que no se ha guardado ningún archivo binario; el único archivo en el directorio es el archivo hello.go que acabamos de crear. 
>
> El comando "go run" compila tu código en un archivo binario temporal. Construye el archivo binario, lo ejecuta desde ese directorio temporal y luego elimina el archivo binario después de que tu programa finalice. Esto hace que el comando "go run" sea útil para probar pequeños programas o para usar Go como un lenguaje de script.
>
#### go build
> La mayoria del tiempo vamos a necesitar construir un fichero binario para luego ejecutar nuestro programa.
```
go build hello.go
```
> El comando anterior crea un fichero binario ejecutable llamado hello en nuestro directorio actual. 
>
> Al ejecutar nuestro programa en la terminal obtenemos lo siguiente:
>
```
./hello
Hello World!
```
>

¿Quieres seguir aprendiendo Go?

Te recomiendo el siguiente recurso [Golang Tour](https://go.dev/tour/welcome/1)
## Instalar Go

Listos para aprender Golang? Vamos 🚀

Página oficial para descargar e instalar Go - [Descargar](https://go.dev/doc/install)

Instalando Go - Linux

Empezamos en nuestro directorio home:
```
$ pwd
/home/gopher
```
Descargamos la última versión de Go:
```
$ wget -q https://golang.org/dl/go1.19.1.linux-$GOARCH.tar.gz
```

Extraemos e Instalamos:
```
$ sudo tar -C /usr/local -xzf go1.19.1.linux-$GOARCH.tar.gz
````
Añadimos el directorio donde se instalo go en nuestro PATH:
```
$ echo export PATH="/usr/local/go/bin:$PATH" >>$HOME/.profile
```

Carga la configuración en tu perfil:
```
$ source $HOME/.profile
````
Verifica la instalación de Go:
```
$ go version
go version go1.19.1 linux/amd64
```
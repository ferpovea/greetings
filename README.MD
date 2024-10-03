# saludos en go
Este paquete proporcina una forma de saludar

## Ejemplo de Uso
package main

import (
	"fmt"
	"log"

	"github.com/ferpovea/greetings"
)

func main() {
	log.SetPrefix("grettings: ")
	log.SetFlags(0)

	names := []string{"Fernando", "Maxi", "Fefi", "Carolina"}

	messages, err := greetings.Hellos(names)

	//message, err := greetings.Hello("Fernando")
	if err != nil {
		log.Fatal(err)
	}
	fmt.Println(messages)
}



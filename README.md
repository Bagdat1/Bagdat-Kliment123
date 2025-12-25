package main

import (
	"fmt"
	"net/http"
)

func main() {
	http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
		fmt.Fprintln(w, "GO Backend жұмыс істеп тұр ✅")
	})

	fmt.Println("Backend 8080 портта іске қосылды")
	http.ListenAndServe(":8080", nil)
}

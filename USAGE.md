<!-- Start SDK Example Usage -->


```go
package main

import (
	"context"
	testupload "github.com/speakeasy-sdks/test-upload"
	"log"
)

func main() {
	s := testupload.New()

	ctx := context.Background()
	res, err := s.Pets.CreatePets(ctx)
	if err != nil {
		log.Fatal(err)
	}

	if res.StatusCode == http.StatusOK {
		// handle response
	}
}

```
<!-- End SDK Example Usage -->
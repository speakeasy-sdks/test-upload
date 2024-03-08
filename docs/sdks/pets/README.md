# Pets
(*Pets*)

### Available Operations

* [CreatePets](#createpets) - Create a pet
* [ListPets](#listpets) - List all pets
* [ShowPetByID](#showpetbyid) - Info for a specific pet

## CreatePets

Create a pet

### Example Usage

```go
package main

import(
	testupload "github.com/speakeasy-sdks/test-upload"
	"context"
	"github.com/speakeasy-sdks/test-upload/pkg/models/shared"
	"log"
)

func main() {
    s := testupload.New()

    ctx := context.Background()
    res, err := s.Pets.CreatePets(ctx, shared.Pet{
        ID: 596804,
        Name: "<value>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |
| `request`                                             | [shared.Pet](../../pkg/models/shared/pet.md)          | :heavy_check_mark:                                    | The request object to use for the request.            |


### Response

**[*operations.CreatePetsResponse](../../pkg/models/operations/createpetsresponse.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |

## ListPets

List all pets

### Example Usage

```go
package main

import(
	testupload "github.com/speakeasy-sdks/test-upload"
	"context"
	"log"
)

func main() {
    s := testupload.New()


    var limit *int = testupload.Int(21453)

    ctx := context.Background()
    res, err := s.Pets.ListPets(ctx, limit)
    if err != nil {
        log.Fatal(err)
    }
    if res.Pets != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |
| `limit`                                               | **int*                                                | :heavy_minus_sign:                                    | How many items to return at one time (max 100)        |


### Response

**[*operations.ListPetsResponse](../../pkg/models/operations/listpetsresponse.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |

## ShowPetByID

Info for a specific pet

### Example Usage

```go
package main

import(
	testupload "github.com/speakeasy-sdks/test-upload"
	"context"
	"log"
)

func main() {
    s := testupload.New()


    var petID string = "<value>"

    ctx := context.Background()
    res, err := s.Pets.ShowPetByID(ctx, petID)
    if err != nil {
        log.Fatal(err)
    }
    if res.Pet != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |
| `petID`                                               | *string*                                              | :heavy_check_mark:                                    | The id of the pet to retrieve                         |


### Response

**[*operations.ShowPetByIDResponse](../../pkg/models/operations/showpetbyidresponse.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |

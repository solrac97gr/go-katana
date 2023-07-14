# Go Katana

This extension is a compilation of all the tools I create for help me in my good projects (Snippets, Code Generator, etc).

## Snippets

### Create a Entity [Snippet:`entity`]

Generate a Entity using the file name.

```go
package models

type Exmaple struct {
	field string
}

func NewExmaple(field string) Exmaple {
	return Exmaple{
		//Add properties
		field: field,
	}
}

func (e Exmaple) Validate() error {
	//TODO: Implement
	return nil
}
```

### Create a Pointer Entity [Snippet:`pentity`]

Generate a Entity using the file name.

```go
package models

type Exmaple struct {
	field string
}

func NewExmaple(field string) *Exmaple {
	return &Exmaple{
		//Add properties
		field: field,
	}
}

func (e *Exmaple) Validate() error {
	//TODO: Implement
	return nil
}
```


### Create a Value Object model [Snippet:`vo`]

Using the snippet `vo` will generate a value object model for Go.

The package will be the name of the folder, the VO name will be the name of the file (user_email.go)

```go
package models

type UserEmail struct {
	value string
}

func NewUserEmail(value string) UserEmail {
	return UserEmail{
		value: value,
	}
}

func (u UserEmail) Equals(other UserEmail) bool {
	return u.value == other.value
}

func (u UserEmail) Validate() error {
	//TODO: Implement
	return nil
}
```

### Create a Port [Snippet:`port`]

Generate a Interface of the current file name

The name of the file its the name of the interface (user_application.go) and the name of the package it's the folder.

```go
package models

type UserApplication interface{}
```
### Create a Implementation [Snippet:`impl`]

Generate a Implementation of a Interface

> We need to write the path of the import.

```go
package query_builder

import (
 ports "auth/internal/query_builder"
)

type QueryBuilder struct {
	field string
}

// Validate the interface it's completed in the struct
var _ ports.QueryBuilder = (*QueryBuilder)(nil)

func NewQueryBuilder(field string) (QueryBuilder, error) {
	return QueryBuilder{
		//Add properties
		field: field,
	},nil
}
```

### Create a Pointer Implementation [Snippet:`pimpl`]

Generate a Implementation of a Interface

> We need to write the path of the import.

```go
package query_builder

import (
 ports "auth/internal/query_builder"
)

type QueryBuilder struct {
	field string
}

// Validate the interface it's completed in the struct
var _ ports.QueryBuilder = (*QueryBuilder)(nil)

func NewQueryBuilder(field string) (*QueryBuilder, error) {
	return &QueryBuilder{
		//Add properties
		field: field,
	},nil
}
```

### Generate Reciver Function [Snippet:`rfunc`]

Generate a reciver function of the current file we are working
- The reciver entity will be take it from the file name like in entity snippet

```go
func (e Entity) FunctionName() error {
	//TODO: Implement
	return nil
}
```

### Generate Pointer Reciver Function [Snippet:`prfunc`]

Generate a reciver function of the current file we are working
- The reciver entity will be take it from the file name like in entity snippet

```go
func (e *Entity) FunctionName() error {
	//TODO: Implement
	return nil
}
```

### Generate only a constructor [Snippet:`constructor`]

Generate a constructor for the entity

```go
func NewEntity(value string) Entity {
	return Entity{
		value: value
	}
}
```

### Generate only a pointer constructor [Snippet:`pconstructor`]

Generate a constructor for the entity

```go
func NewEntity(value string) *Entity {
	return &Entity{
		value: value
	}
}
```
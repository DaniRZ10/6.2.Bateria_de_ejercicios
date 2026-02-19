# Ejercicio 1: Usuario de Streaming

## Diagrama de Clases

```mermaid
classDiagram
    class Usuario {
        -String nombre
        -String password
        +String email
        +cambiarPassword(String nueva) string
        -validarEmail() void
    }
```



# Ejercicio 2: Sistema Escolar

## Diagrama de Clases

```mermaid
classDiagram
    class Persona {
        -String nombre
        -String dni
    }
    class Estudiante {
        -String numeroExpediente
        -double notaMedia
    }
    Persona <|-- Estudiante
```


# Ejercicio 3: Computadora

## Diagrama de Clases

```mermaid
classDiagram
    class Computadora 
    class PlacaBase
    class Raton
    
    Computadora *-- PlacaBase : Composición (Fuerte)
    Computadora o-- Raton : Agregación (Débil)
```



# Ejercicio 4: Centro Comercial

## Diagrama de Clases

```mermaid
classDiagram
    class CentroComercial 
    class Tienda 
    CentroComercial "1" -- "1..*" Tienda : alberga
```



# Ejercicio 5: Sistema de Pagos

## Diagrama de Clases

```mermaid
classDiagram
    class MetodoPago {
        <<interface>>
        +procesar(double importe)
    }
    class Tarjeta 
    class Paypal 
    class Carrito {
        +pagar(MetodoPago miMetodo)
    }
    MetodoPago <|.. Tarjeta
    MetodoPago <|.. Paypal
    Carrito ..> MetodoPago : usa
```



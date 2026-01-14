# Conceptual models

## Ezcream example from lecture note

**Conceptual ERD**

<img src = "ezcream_example.png" width = 500>

**Relationship statements**
- A Customer places *one or many* Orders
- An Order is placed by *one and only one* Customer
- An Order contains *one or many* Products
- A Product is contained in *zero or many* Orders


Customer(customer_id, first_name, last_name, ...)
...
# typescript-crud
crud using typescript and bootstrap



## mermaid

~~~mermaid
flowchart TD
    A[Start] --> B{Is it?}
    B -- Yes --> C[OK]
    C --> D[Rethink]
    D --> B
    B -- No ----> E[End]
~~~

- doc: [http://mermaid.js.org/syntax/flowchart.html]
- [https://www.mermaidflow.app/]
- [**COOL**] [https://mermaid.live/]

- another:

~~~mermaid
erDiagram
    User {
        UserID
        UserName
        Password
        FirstName
        LastName
        Email
        Role
    }
    Department {
        DeptID
        DepartmentName
        Location
    }
    Product {
        ProductID
        ProductName
        Description
        UnitPrice
    }
    SaleOrder {
        OrderID
        OrderDate
        CustomerName
        TotalAmount
    }
    Inventory {
        InventoryID
        ProductID
        QuantityInStock
    }
    User --|{ Belongs to }|-- Department : WorksIn
    User --|{ Created by }|-- SaleOrder : Created
    SaleOrder --|{ Contains }|-- Product : Includes
    Product --|{ Managed by }|-- Inventory : ManagedBy
~~~

## another

~~~mermaid
mindmap
  root((Products))
    Origins
      Food
      ::icon(fa fa-book)
      Clothes
        Products
    Logistic
      On effectiveness<br/>and features
      On Automatic creation
        Uses
            Warehouse 1
            Point of Sale
            Human Capital
    Tools
      Workforce and machines
      Other Tools
~~~



~~~mermaid
---
title: Order example
---
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
~~~

~~~mermaid
erDiagram
    vendor {
        type field
        string Name
        string Contact_Information
    }
    transaction {
        transactionID PK
        string Type
        datetime Date
        int Quantity
    }
    org ||--o{ user : "Many-to-One"
    org ||--o{ dept : "Many-to-One"
    dept ||--o{ emp : "Many-to-One"
    vendor ||--o{ po : "Many-to-One"
    po ||--o{ po_item : "One-to-Many"
    product ||--o{ po_item : "Many-to-One"
    product ||--o{ inventory : "Many-to-One"
    customer ||--o{ so : "Many-to-One"
    so ||--o{ so_item : "One-to-Many"
    product ||--o{ so_item : "Many-to-One"
    product ||--o{ transaction : "Many-to-One"
    vendor ||--o{ transaction : "Many-to-One"
    customer ||--o{ transaction : "Many-to-One"
    user ||--o{ transaction : "Many-to-One"
~~~


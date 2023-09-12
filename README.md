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
    org {
        Org_ID PrimKey
        Name string
        Address string
        Phone string
        Email string
    }
    user {
        UserID int
        FirstName string
        LastName string
        Username string
        Password string
        Email string
        Role string
    }
    dept {
        Dept_ID PrimKey
        Name asd
        Description asd
        Location asd
    }
    empl {
        Emp_ID PrimKey
        First Name
        Last Name
        Dateof Birth
        Contact Information
    }
    product {
        Product_ID PrimKey
        Name string
        Description string
        SKU string
        Price string
        Quantity string
    }
    vendor {
        Vendor_ID PrimKey
        Name string
        Contact Information
    }
    po {
        PO_ID PrimKey
        Date Date
        Total Amount
        Status string
    }
    po_item {
        Line_Item_ID PrimKey
        Quantity int
        Unit Price
        Total Price
    }
    customer {
        Customer_ID PrimKey
        Name string
        Contact Information
        Billing Address
        Shipping Address
    }
    so {
        SO_ID PrimKey
        Date Date
        Total Amount
        Status string
    }
    so_item {
        Line_Item_ID PrimKey
        Quantity int
        Unit Price
        Total Price
    }
    inventory {
        Inventory_ID PrimKey
        Quantity int
        Location geo
        LastUpdated Date
    }
    transaction {
        Transaction_ID PrimKey
        Type string
        Date date
        Quantity int
    }


    org ||--o{ user : "Many-to-One"
    org ||--o{ dept : "Many-to-One"
    dept ||--o{ empl : "Many-to-One"
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


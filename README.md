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
- erDiagrams [https://newdevsguide.com/2023/04/08/creating-erds-with-mermaid/]

- another:

~~~mermaid
erDiagram
    User {
        Userid int
        UserName string
        Password string
        FirstName string
        LastName string
        Email string
        Role string
    }
    Department {
        Deptid string
        DepartmentName string
        Location string
    }
    Product {
        Productid int
        ProductName string
        Description string
        UnitPrice string
    }
    SaleOrder {
        Orderid string
        OrderDate string
        CustomerName string
        TotalAmount string
    }
    Inventory {
        Inventoryid string
        Productid string
        QuantityInStock string
    }
    User ||-- |{ Department : WorksIn-BelongsTo
    User ||--|{ SaleOrder : CreatedBy
    SaleOrder }|--|{ Product : IncludesContains
    Product }|--|{ Inventory : ManagedBy
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

~~~mermaid
flowchart TD
    subgraph ComponentDataFlow
        odx2[ChildComponent]-- Data<br>@Output() --> odx1
        odx1[ParentComponent]-- Data<br>@Input() --> odx2
    end
~~~


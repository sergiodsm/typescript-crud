# typescript-crud
crud using typescript and bootstrap



## test


~~~mermaid
stateDiagram-v2
    state Platzi-courses {
        state School {
            [*] --> Course 
            state Course {
                [*] --> exam : (folder)
                [*] --> exercise: (folder)
                exercise --> scripts
                [*] --> imgs: (folder)
                [*] --> shared: (folder)
                shared --> slides: (presentation file)
                [*] --> README:(summary file)
            }
        }
        [*] --> Certificates
        state Certificates{
            [*] --> certificate: (file)
        }
    } 
~~~

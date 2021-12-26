# react_hw1_ex9


## Пример ссылки 

[LinkExample](https://github.com/garlife/react_hw1_ex1)

## PlantUml

![plantUml](https://trello-attachments.s3.amazonaws.com/607a4f1910a1f27254381596/607a520b7cd92579e31ac9c6/cb276a837091193a7a8c20ac9ddceb61/image.png)

## plantumlcode

```plantumlcode
@startuml packaging
component "Create-project-app" as project  {

    folder "/node_modues" {
        artifact "/..." as node_modules
    }
    folder "/src" {
        artifact "/..." as src
    }
    folder "/public/..." as public {
        file "/index.html" as public_index
        file "/favicon.ico" as public_favicon
        file "/manifest.json" as public_manifest
    }
}

cloud {
    card "localhost:3000" {
        file "manifest.json" as manifest
        file "main.chunk.js" as main
        file "favicon.ico" as favicon
        file "vendor~main.chunk.js" as vendor
        file "bundle.js" as bundle

        node_modules --> vendor
        src --> main
        public_favicon --> favicon
        public_manifest --> manifest

        artifact "index.html" as index {
            public_index --> index
            manifest --> index
            main --> index
            favicon --> index
            vendor --> index
            bundle -r-> index
        }
    }
}
@enduml

```

## Таблица

Заголовок1 | Заголовок2
--------|--------
Ячейка1 |Ячейка2


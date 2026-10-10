---
title: "Aspose::Words::Tables::Cell::get_PreviousCell método"
linktitle: "get_PreviousCell"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Cell::get_PreviousCell método. Obtiene el nodo Cell anterior en C++."
type: docs
weight: 12500
url: /es/cpp/aspose.words.tables/cell/get_previouscell/
---
## Cell::get_PreviousCell method


Obtiene el nodo [Cell](../) anterior.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::Tables::Cell::get_PreviousCell()
```


## Ejemplos



Muestra cómo enumerar todas las celdas de la tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Enumere todas las celdas de la tabla.
for (System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_FirstRow(); row != nullptr; row = row->get_NextRow())
{
    for (System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_FirstCell(); cell != nullptr; cell = cell->get_NextCell())
    {
        std::cout << cell->GetText() << std::endl;
    }
}
```

## Ver también

* Class [Cell](../)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

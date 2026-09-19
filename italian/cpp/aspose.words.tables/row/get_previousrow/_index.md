---
title: "Metodo Aspose::Words::Tables::Row::get_PreviousRow"
linktitle: "get_PreviousRow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::Row::get_PreviousRow. Ottiene il nodo Row precedente in C++."
type: docs
weight: 11500
url: /it/cpp/aspose.words.tables/row/get_previousrow/
---
## Row::get_PreviousRow method


Ottiene il nodo [Row](../) precedente.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Row::get_PreviousRow()
```


## Esempi



Mostra come enumerare tutte le celle della tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Enumera tutte le celle della tabella.
for (System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_FirstRow(); row != nullptr; row = row->get_NextRow())
{
    for (System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_FirstCell(); cell != nullptr; cell = cell->get_NextCell())
    {
        std::cout << cell->GetText() << std::endl;
    }
}
```

## Vedi anche

* Class [Row](../)
* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

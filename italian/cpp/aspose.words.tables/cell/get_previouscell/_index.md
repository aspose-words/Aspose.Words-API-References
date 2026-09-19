---
title: "Metodo Aspose::Words::Tables::Cell::get_PreviousCell"
linktitle: "get_PreviousCell"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::Cell::get_PreviousCell. Ottiene il nodo Cell precedente in C++."
type: docs
weight: 12500
url: /it/cpp/aspose.words.tables/cell/get_previouscell/
---
## Cell::get_PreviousCell method


Ottiene il nodo [Cell](../) precedente.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::Tables::Cell::get_PreviousCell()
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

* Class [Cell](../)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

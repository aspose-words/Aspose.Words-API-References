---
title: "Aspose::Words::Tables::Cell::get_NextCell metodo"
linktitle: "get_NextCell"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Cell::get_NextCell metodo. Ottiene il nodo Cell successivo in C++."
type: docs
weight: 9500
url: /it/cpp/aspose.words.tables/cell/get_nextcell/
---
## Cell::get_NextCell method


Ottiene il nodo [Cell](../) successivo.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::Tables::Cell::get_NextCell()
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

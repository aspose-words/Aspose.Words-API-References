---
title: "Aspose::Words::Tables::Cell::get_PreviousCell metod"
linktitle: "get_PreviousCell"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Cell::get_PreviousCell metod. Hämtar föregående Cell‑nod i C++."
type: docs
weight: 12500
url: /sv/cpp/aspose.words.tables/cell/get_previouscell/
---
## Cell::get_PreviousCell method


Hämtar föregående [Cell](../) nod.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::Tables::Cell::get_PreviousCell()
```


## Exempel



Visar hur man enumererar genom alla tabellceller.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Enumerera genom alla celler i tabellen.
for (System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_FirstRow(); row != nullptr; row = row->get_NextRow())
{
    for (System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_FirstCell(); cell != nullptr; cell = cell->get_NextCell())
    {
        std::cout << cell->GetText() << std::endl;
    }
}
```

## Se även

* Class [Cell](../)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

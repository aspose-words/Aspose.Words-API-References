---
title: "Aspose::Words::Tables::Cell::get_PreviousCell-Methode"
linktitle: "get_PreviousCell"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Cell::get_PreviousCell-Methode. Ruft den vorherigen Cell-Knoten in C++ ab."
type: docs
weight: 12500
url: /de/cpp/aspose.words.tables/cell/get_previouscell/
---
## Cell::get_PreviousCell method


Ruft den vorherigen [Cell](../)-Knoten ab.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::Tables::Cell::get_PreviousCell()
```


## Beispiele



Zeigt, wie man durch alle Tabellenzellen iteriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Iteriere durch alle Zellen der Tabelle.
for (System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_FirstRow(); row != nullptr; row = row->get_NextRow())
{
    for (System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_FirstCell(); cell != nullptr; cell = cell->get_NextCell())
    {
        std::cout << cell->GetText() << std::endl;
    }
}
```

## Siehe auch

* Class [Cell](../)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Tables::Cell::get_NextCell Methode"
linktitle: "get_NextCell"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Cell::get_NextCell Methode. Gibt den nächsten Cell-Knoten in C++ zurück."
type: docs
weight: 9500
url: /de/cpp/aspose.words.tables/cell/get_nextcell/
---
## Cell::get_NextCell method


Gibt den nächsten [Cell](../) Knoten zurück.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::Tables::Cell::get_NextCell()
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

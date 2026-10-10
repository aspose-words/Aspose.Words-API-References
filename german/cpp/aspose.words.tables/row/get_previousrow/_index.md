---
title: "Aspose::Words::Tables::Row::get_PreviousRow Methode"
linktitle: "get_PreviousRow"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Row::get_PreviousRow Methode. Gibt den vorherigen Row-Knoten in C++ zurück."
type: docs
weight: 11500
url: /de/cpp/aspose.words.tables/row/get_previousrow/
---
## Row::get_PreviousRow method


Gibt den vorherigen [Row](../)-Knoten zurück.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Row::get_PreviousRow()
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

* Class [Row](../)
* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

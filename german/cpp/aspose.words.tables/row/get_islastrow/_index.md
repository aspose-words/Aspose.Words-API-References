---
title: "Aspose::Words::Tables::Row::get_IsLastRow Methode"
linktitle: "get_IsLastRow"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Row::get_IsLastRow Methode. Wahr, wenn dies die letzte Zeile in einer Tabelle ist; andernfalls falsch in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.tables/row/get_islastrow/
---
## Row::get_IsLastRow method


Wahr, wenn dies die letzte Zeile in einer Tabelle ist; andernfalls falsch.

```cpp
bool Aspose::Words::Tables::Row::get_IsLastRow()
```


## Beispiele



Zeigt, wie man eine Tabelle so einstellt, dass sie auf derselben Seite zusammenbleibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Aktivieren von KeepWithNext für jeden Absatz in der Tabelle, außer für die
// letzten in der letzten Zeile verhindern, dass die Tabelle über mehrere Seiten hinweg aufgeteilt wird.
for (auto&& cell : System::IterateOver<Aspose::Words::Tables::Cell>(table->GetChildNodes(Aspose::Words::NodeType::Cell, true)))
{
    for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(cell->get_Paragraphs()))
    {
        ASSERT_TRUE(para->get_IsInCell());

        if (!(cell->get_ParentRow()->get_IsLastRow() && para->get_IsEndOfCell()))
        {
            para->get_ParagraphFormat()->set_KeepWithNext(true);
        }
    }
}

doc->Save(get_ArtifactsDir() + u"Table.KeepTableTogether.docx");
```

## Siehe auch

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

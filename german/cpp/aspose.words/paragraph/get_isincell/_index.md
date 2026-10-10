---
title: "Aspose::Words::Paragraph::get_IsInCell Methode"
linktitle: "get_IsInCell"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Paragraph::get_IsInCell Methode. True, wenn dieser Absatz ein unmittelbares Kind von Cell ist; false andernfalls in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words/paragraph/get_isincell/
---
## Paragraph::get_IsInCell method


True, wenn dieser Absatz ein unmittelbares Kind von [Cell](../../../aspose.words.tables/cell/) ist; false andernfalls.

```cpp
bool Aspose::Words::Paragraph::get_IsInCell()
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

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

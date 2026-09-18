---
title: "Aspose::Words::ParagraphFormat::get_KeepWithNext Methode"
linktitle: "get_KeepWithNext"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_KeepWithNext Methode. Wahr, wenn der Absatz auf derselben Seite bleiben soll wie der nachfolgende Absatz in C++."
type: docs
weight: 18000
url: /de/cpp/aspose.words/paragraphformat/get_keepwithnext/
---
## ParagraphFormat::get_KeepWithNext method


Wahr, wenn der Absatz auf derselben Seite wie der nachfolgende Absatz bleiben soll.

```cpp
bool Aspose::Words::ParagraphFormat::get_KeepWithNext()
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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

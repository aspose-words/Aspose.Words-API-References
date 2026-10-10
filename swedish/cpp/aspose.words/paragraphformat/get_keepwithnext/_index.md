---
title: "Aspose::Words::ParagraphFormat::get_KeepWithNext metod"
linktitle: "get_KeepWithNext"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_KeepWithNext metod. Sant om stycket ska förbli på samma sida som stycket som följer efter det i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words/paragraphformat/get_keepwithnext/
---
## ParagraphFormat::get_KeepWithNext method


Sant om stycket ska förbli på samma sida som stycket som följer efter det.

```cpp
bool Aspose::Words::ParagraphFormat::get_KeepWithNext()
```


## Exempel



Visar hur man ställer in en tabell så att den hålls ihop på samma sida.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Aktivera KeepWithNext för varje stycke i tabellen förutom för den
// de sista i den sista raden kommer att förhindra att tabellen delas upp över flera sidor.
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

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Paragraph::get_IsEndOfCell metodu"
linktitle: "get_IsEndOfCell"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::get_IsEndOfCell metodu. C++'ta bu paragraf bir Hücre'deki son paragraf ise True; aksi takdirde false."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/paragraph/get_isendofcell/
---
## Paragraph::get_IsEndOfCell method


Bu paragraf bir [Cell](../../../aspose.words.tables/cell/) içindeki son paragraf ise True; aksi takdirde false.

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfCell()
```


## Örnekler



Bir tablonun aynı sayfada birlikte kalmasını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Tablodaki her paragraf için KeepWithNext'i etkinleştirmek, ancak
// son satırdaki son öğeler, tablonun birden fazla sayfaya bölünmesini önleyecektir.
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

## Ayrıca Bakınız

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

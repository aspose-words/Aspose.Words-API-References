---
title: "Aspose::Words::Paragraph::get_IsInCell yöntemi"
linktitle: "get_IsInCell"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::get_IsInCell yöntemi. Bu paragraf bir Cell'in doğrudan çocuğu ise Doğru; aksi takdirde C++'da Yanlış."
type: docs
weight: 13000
url: /tr/cpp/aspose.words/paragraph/get_isincell/
---
## Paragraph::get_IsInCell method


Doğru ise bu paragraf bir [Cell](../../../aspose.words.tables/cell/) doğrudan çocuğu; aksi takdirde Yanlış.

```cpp
bool Aspose::Words::Paragraph::get_IsInCell()
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

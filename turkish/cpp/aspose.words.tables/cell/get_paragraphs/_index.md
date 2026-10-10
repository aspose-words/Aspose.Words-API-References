---
title: "Aspose::Words::Tables::Cell::get_Paragraphs yöntemi"
linktitle: "get_Paragraphs"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Cell::get_Paragraphs yöntemi. C++'de hücrenin doğrudan alt öğeleri olan paragraf koleksiyonunu alır."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.tables/cell/get_paragraphs/
---
## Cell::get_Paragraphs method


Hücrenin doğrudan çocukları olan paragraf koleksiyonunu alır.

```cpp
System::SharedPtr<Aspose::Words::ParagraphCollection> Aspose::Words::Tables::Cell::get_Paragraphs()
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

* Class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

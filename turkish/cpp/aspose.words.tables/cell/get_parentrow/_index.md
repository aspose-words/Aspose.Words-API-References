---
title: "Aspose::Words::Tables::Cell::get_ParentRow yöntemi"
linktitle: "get_ParentRow"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Cell::get_ParentRow yöntemi. C++'de hücrenin üst satırını döndürür."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.tables/cell/get_parentrow/
---
## Cell::get_ParentRow method


Hücrenin üst satırını döndürür.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Cell::get_ParentRow()
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

* Class [Row](../../row/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

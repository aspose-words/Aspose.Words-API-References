---
title: "Aspose::Words::Tables::Row::get_IsLastRow yöntemi"
linktitle: "get_IsLastRow"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Row::get_IsLastRow yöntemi. Bu bir tablodaki son satır ise True, aksi takdirde false döndürür C++'de."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.tables/row/get_islastrow/
---
## Row::get_IsLastRow method


Bir tabloda bu son satırsa doğru; aksi takdirde yanlış.

```cpp
bool Aspose::Words::Tables::Row::get_IsLastRow()
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

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

---
title: Aspose::Words::Tables::Row::get_IsLastRow method
linktitle: get_IsLastRow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Row::get_IsLastRow method. True if this is the last row in a table; false otherwise in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.tables/row/get_islastrow/
---
## Row::get_IsLastRow method


True if this is the last row in a table; false otherwise.

```cpp
bool Aspose::Words::Tables::Row::get_IsLastRow()
```


## Examples



Shows how to set a table to stay together on the same page. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Enabling KeepWithNext for every paragraph in the table except for the
// last ones in the last row will prevent the table from splitting across multiple pages.
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

## See Also

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

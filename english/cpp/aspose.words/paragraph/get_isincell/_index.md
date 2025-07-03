---
title: Aspose::Words::Paragraph::get_IsInCell method
linktitle: get_IsInCell
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Paragraph::get_IsInCell method. True if this paragraph is an immediate child of Cell; false otherwise in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words/paragraph/get_isincell/
---
## Paragraph::get_IsInCell method


True if this paragraph is an immediate child of [Cell](../../../aspose.words.tables/cell/); false otherwise.

```cpp
bool Aspose::Words::Paragraph::get_IsInCell()
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

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: get_IsEndOfCell
second_title: Aspose.Words for C++ API Reference
description: True if this paragraph is the last paragraph in a Cell; false otherwise.
type: docs
weight: 79
url: /cpp/aspose.words/paragraph/get_isendofcell/
---
## Paragraph::get_IsEndOfCell method


True if this paragraph is the last paragraph in a [Cell](../../../aspose.words.tables/cell/); false otherwise.

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfCell()
```


## Examples



Shows how to set a table to stay together on the same page. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Table spanning two pages.docx");
SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Enabling KeepWithNext for every paragraph in the table except for the
// last ones in the last row will prevent the table from splitting across multiple pages.
for (const auto& cell : System::IterateOver(table->GetChildNodes(NodeType::Cell, true)->LINQ_OfType<SharedPtr<Cell>>()))
{
    for (const auto& para : System::IterateOver(cell->get_Paragraphs()->LINQ_OfType<SharedPtr<Paragraph>>()))
    {
        ASSERT_TRUE(para->get_IsInCell());

        if (!(cell->get_ParentRow()->get_IsLastRow() && para->get_IsEndOfCell()))
        {
            para->get_ParagraphFormat()->set_KeepWithNext(true);
        }
    }
}

doc->Save(ArtifactsDir + u"Table.KeepTableTogether.docx");
```

## See Also

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)

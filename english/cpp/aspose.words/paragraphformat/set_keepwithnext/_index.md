---
title: Aspose::Words::ParagraphFormat::set_KeepWithNext method
linktitle: set_KeepWithNext
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::set_KeepWithNext method. True if the paragraph is to remains on the same page as the paragraph that follows it in C++.'
type: docs
weight: 57000
url: /cpp/aspose.words/paragraphformat/set_keepwithnext/
---
## ParagraphFormat::set_KeepWithNext method


True if the paragraph is to remains on the same page as the paragraph that follows it.

```cpp
void Aspose::Words::ParagraphFormat::set_KeepWithNext(bool value)
```

## Examples


Shows how to set a table to stay together on the same page.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Table spanning two pages.docx"));
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Enabling KeepWithNext for every paragraph in the table except for the
// last ones in the last row will prevent the table from splitting across multiple pages.
for (auto&& cell : System::IterateOver<Aspose::Words::Tables::Cell>(table->GetChildNodes(NodeType::Cell, true)))
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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

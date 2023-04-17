---
title: Aspose::Words::TabStop::get_Position method
linktitle: get_Position
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TabStop::get_Position method. Gets the position of the tab stop in points in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/tabstop/get_position/
---
## TabStop::get_Position method


Gets the position of the tab stop in points.

```cpp
double Aspose::Words::TabStop::get_Position()
```


## Examples



Shows how to modify the position of the right tab stop in TOC related paragraphs. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Table of contents.docx");

// Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
for (const auto& para : System::IterateOver(doc->GetChildNodes(NodeType::Paragraph, true)->LINQ_OfType<SharedPtr<Paragraph>>()))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= StyleIdentifier::Toc1 &&
        para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= StyleIdentifier::Toc9)
    {
        // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
        SharedPtr<TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // Replace the first default tab, stop with a custom tab stop.
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(ArtifactsDir + u"Styles.ChangeTocsTabStops.docx");
```

## See Also

* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

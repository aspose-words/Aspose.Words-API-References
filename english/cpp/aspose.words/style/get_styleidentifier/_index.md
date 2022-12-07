---
title: get_StyleIdentifier
second_title: Aspose.Words for C++ API Reference
description: Gets the locale independent style identifier for a built-in style.
type: docs
weight: 196
url: /cpp/aspose.words/style/get_styleidentifier/
---
## Style::get_StyleIdentifier method


Gets the locale independent style identifier for a built-in style.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Style::get_StyleIdentifier() const
```

## Remarks


For user defined (custom) styles, this property returns [User](../../styleidentifier/).

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

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)

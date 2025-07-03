---
title: Aspose::Words::TabStopCollection::RemoveByPosition method
linktitle: RemoveByPosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TabStopCollection::RemoveByPosition method. Removes a tab stop at the specified position from the collection in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection::RemoveByPosition method


Removes a tab stop at the specified position from the collection.

```cpp
void Aspose::Words::TabStopCollection::RemoveByPosition(double position)
```


| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The position (in points) of the tab stop to remove. |

## Examples



Shows how to modify the position of the right tab stop in TOC related paragraphs. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table of contents.docx");

// Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= Aspose::Words::StyleIdentifier::Toc1 && para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= Aspose::Words::StyleIdentifier::Toc9)
    {
        // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
        System::SharedPtr<Aspose::Words::TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // Replace the first default tab, stop with a custom tab stop.
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(get_ArtifactsDir() + u"Styles.ChangeTocsTabStops.docx");
```

## See Also

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

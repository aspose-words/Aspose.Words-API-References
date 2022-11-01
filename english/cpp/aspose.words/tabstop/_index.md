---
title: TabStop
second_title: Aspose.Words for C++ API Reference
description: Represents a single custom tab stop. The TabStop object is a member of the TabStopCollection collection.
type: docs
weight: 872
url: /cpp/aspose.words/tabstop/
---
## TabStop class


Represents a single custom tab stop. The **TabStop** object is a member of the [TabStopCollection](../tabstopcollection/) collection.

```cpp
class TabStop : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Compares with the specified [TabStop](./). |
| [get_Alignment](./get_alignment/)() const | Gets or sets the alignment of text at this tab stop. |
| [get_IsClear](./get_isclear/)() | Returns true if this tab stop clears any existing tab stops in this position. |
| [get_Leader](./get_leader/)() const | Gets or sets the type of the leader line displayed under the tab character. |
| [get_Position](./get_position/)() | Gets the position of the tab stop in points. |
| [GetHashCode](./gethashcode/)() const override | Calculates hash code for this object. |
| [set_Alignment](./set_alignment/)(Aspose::Words::TabAlignment) | Setter for [Aspose::Words::TabStop::get_Alignment](./get_alignment/). |
| [set_Leader](./set_leader/)(Aspose::Words::TabLeader) | Setter for [Aspose::Words::TabStop::get_Leader](./get_leader/). |
| [TabStop](./tabstop/)(double) | Initializes a new instance of this class. |
| [TabStop](./tabstop/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Initializes a new instance of this class. |

Normally, a tab stop specifies a position where a tab stop exists. But because tab stops can be inherited from parent styles, it might be needed for the child object to define explicitly that there is no tab stop at a given position. To clear an inherited tab stop at a given position, create a **TabStop** object and set [Alignment](./get_alignment/) to **TabAlignment.Clear**.

For more information see [TabStopCollection](../tabstopcollection/).

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


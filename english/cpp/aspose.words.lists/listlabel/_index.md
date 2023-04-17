---
title: Aspose::Words::Lists::ListLabel class
linktitle: ListLabel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListLabel class. Defines properties specific to a list label. To learn more, visit the  documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.lists/listlabel/
---
## ListLabel class


Defines properties specific to a list label. To learn more, visit the [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/) documentation article.

```cpp
class ListLabel : public Aspose::Words::IRunAttrSource
```

## Methods

| Method | Description |
| --- | --- |
| [get_Font](./get_font/)() | Gets the list label font. |
| [get_LabelString](./get_labelstring/)() | Gets a string representation of list label. |
| [get_LabelValue](./get_labelvalue/)() | Gets a numeric value for this label. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Examples



Shows how to extract the list labels of all paragraphs that are list items. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");
doc->UpdateListLabels();

SharedPtr<NodeCollection> paras = doc->GetChildNodes(NodeType::Paragraph, true);

// Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
// which start at three and ends at six.
for (auto paragraph : System::IterateOver(
         paras->LINQ_OfType<SharedPtr<Paragraph>>()->LINQ_Where([](SharedPtr<Paragraph> p) { return p->get_ListFormat()->get_IsListItem(); })))
{
    std::cout << "List item paragraph #" << paras->IndexOf(paragraph) << std::endl;

    // This is the text we get when getting when we output this node to text format.
    // This text output will omit list labels. Trim any paragraph formatting characters.
    String paragraphText = paragraph->ToString(SaveFormat::Text).Trim();
    std::cout << "\tExported Text: " << paragraphText << std::endl;

    SharedPtr<ListLabel> label = paragraph->get_ListLabel();

    // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
    // this will tell us what position it is on that level.
    std::cout << "\tNumerical Id: " << label->get_LabelValue() << std::endl;

    // Combine them together to include the list label with the text in the output.
    std::cout << "\tList label combined with text: " << label->get_LabelString() << " " << paragraphText << std::endl;
}
```

## See Also

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)

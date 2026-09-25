---
title: Aspose::Words::Lists::ListLabel::get_LabelString method
linktitle: get_LabelString
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListLabel::get_LabelString method. Gets a string representation of list label in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.lists/listlabel/get_labelstring/
---
## ListLabel::get_LabelString method


Gets a string representation of list label.

```cpp
System::String Aspose::Words::Lists::ListLabel::get_LabelString()
```


## Examples



Shows how to extract the list labels of all paragraphs that are list items. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
// which start at three and ends at six.
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph>>()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    System::Console::WriteLine(System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)));

    // This is the text we get when getting when we output this node to text format.
    // This text output will omit list labels. Trim any paragraph formatting characters.
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    System::Console::WriteLine(System::String::Format(u"\tExported Text: {0}", paragraphText));

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
    // this will tell us what position it is on that level.
    System::Console::WriteLine(System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()));

    // Combine them together to include the list label with the text in the output.
    System::Console::WriteLine(System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText));
}
```

## See Also

* Class [ListLabel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)

---
title: Aspose::Words::Document::UpdateListLabels method
linktitle: UpdateListLabels
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::UpdateListLabels method. Updates list labels for all list items in the document in C++.'
type: docs
weight: 97000
url: /cpp/aspose.words/document/updatelistlabels/
---
## Document::UpdateListLabels method


Updates list labels for all list items in the document.

```cpp
void Aspose::Words::Document::UpdateListLabels()
```

## Remarks


This method updates list label properties such as [LabelValue](../../../aspose.words.lists/listlabel/get_labelvalue/) and [LabelString](../../../aspose.words.lists/listlabel/get_labelstring/) for each [ListLabel](../../paragraph/get_listlabel/) object in the document.

Also, this method is sometimes implicitly called when updating fields in the document. This is required because some fields that may reference list numbers (such as TOC or REF) need them be up-to-date.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

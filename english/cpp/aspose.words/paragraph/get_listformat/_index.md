---
title: Aspose::Words::Paragraph::get_ListFormat method
linktitle: get_ListFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Paragraph::get_ListFormat method. Provides access to the list formatting properties of the paragraph in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words/paragraph/get_listformat/
---
## Paragraph::get_ListFormat method


Provides access to the list formatting properties of the paragraph.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListFormat> Aspose::Words::Paragraph::get_ListFormat()
```


## Examples



Shows how to output all paragraphs in a document that are list items. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Bulleted list item 1");
builder->Writeln(u"Bulleted list item 2");
builder->Writeln(u"Bulleted list item 3");
builder->get_ListFormat()->RemoveNumbers();

SharedPtr<NodeCollection> paras = doc->GetChildNodes(NodeType::Paragraph, true);

for (auto para : System::IterateOver(
         paras->LINQ_OfType<SharedPtr<Paragraph>>()->LINQ_Where([](SharedPtr<Paragraph> p) { return p->get_ListFormat()->get_IsListItem(); })))
{
    std::cout << String::Format(u"This paragraph belongs to list ID# {0}, number style \"{1}\"", para->get_ListFormat()->get_List()->get_ListId(),
                                para->get_ListFormat()->get_ListLevel()->get_NumberStyle())
              << std::endl;
    std::cout << "\t\"" << para->GetText().Trim() << "\"" << std::endl;
}
```

## See Also

* Class [ListFormat](../../../aspose.words.lists/listformat/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

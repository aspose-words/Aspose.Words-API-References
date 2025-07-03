---
title: Aspose::Words::CompositeNode::GetText method
linktitle: GetText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::GetText method. Gets the text of this node and of all its children in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/compositenode/gettext/
---
## CompositeNode::GetText method


Gets the text of this node and of all its children.

```cpp
System::String Aspose::Words::CompositeNode::GetText() override
```

## Remarks


The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).

## Examples



Shows the difference between calling the GetText and ToString methods on a node. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText will retrieve the visible text as well as field codes and special characters.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015", doc->GetText().Trim());

// ToString will give us the document's appearance if saved to a passed save format.
ASSERT_EQ(u"«Field»", doc->ToString(Aspose::Words::SaveFormat::Text).Trim());
```


Shows how to output all paragraphs in a document that are list items. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

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

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

for (auto&& para : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"This paragraph belongs to list ID# {0}, number style \"{1}\"", para->get_ListFormat()->get_List()->get_ListId(), para->get_ListFormat()->get_ListLevel()->get_NumberStyle()) << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\"", para->GetText().Trim()) << std::endl;
}
```

## See Also

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

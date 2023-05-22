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
auto doc = MakeObject<Document>();

auto builder = MakeObject<DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText will retrieve the visible text as well as field codes and special characters.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc->GetText());

// ToString will give us the document's appearance if saved to a passed save format.
ASSERT_EQ(u"«Field»\r\n", doc->ToString(SaveFormat::Text));
```


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

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

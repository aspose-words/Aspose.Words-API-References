---
title: Aspose::Words::CompositeNode::get_LastChild method
linktitle: get_LastChild
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::get_LastChild method. Gets the last child of the node in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/compositenode/get_lastchild/
---
## CompositeNode::get_LastChild method


Gets the last child of the node.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_LastChild() const
```


## Examples



Shows how to use of methods of [Node](../../node/) and [CompositeNode](../) to remove a section before the last section in the document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Section 1 text.");
builder->InsertBreak(BreakType::SectionBreakContinuous);
builder->Writeln(u"Section 2 text.");

// Both sections are siblings of each other.
auto lastSection = System::DynamicCast<Section>(doc->get_LastChild());
auto firstSection = System::DynamicCast<Section>(lastSection->get_PreviousSibling());

// Remove a section based on its sibling relationship with another section.
if (lastSection->get_PreviousSibling() != nullptr)
{
    doc->RemoveChild(firstSection);
}

// The section we removed was the first one, leaving the document with only the second.
ASSERT_EQ(u"Section 2 text.", doc->GetText().Trim());
```

## See Also

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

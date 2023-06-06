---
title: Aspose::Words::Node::get_PreviousSibling method
linktitle: get_PreviousSibling
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Node::get_PreviousSibling method. Gets the node immediately preceding this node in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words/node/get_previoussibling/
---
## Node::get_PreviousSibling method


Gets the node immediately preceding this node.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_PreviousSibling()
```


## Examples



Shows how to use of methods of [Node](../) and [CompositeNode](../../compositenode/) to remove a section before the last section in the document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Section 1 text.");
builder->InsertBreak(BreakType::SectionBreakContinuous);
builder->Writeln(u"Section 2 text.");

// Both sections are siblings of each other.
auto lastSection = System::ExplicitCast<Section>(doc->get_LastChild());
auto firstSection = System::ExplicitCast<Section>(lastSection->get_PreviousSibling());

// Remove a section based on its sibling relationship with another section.
if (lastSection->get_PreviousSibling() != nullptr)
{
    doc->RemoveChild(firstSection);
}

// The section we removed was the first one, leaving the document with only the second.
ASSERT_EQ(u"Section 2 text.", doc->GetText().Trim());
```

## See Also

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

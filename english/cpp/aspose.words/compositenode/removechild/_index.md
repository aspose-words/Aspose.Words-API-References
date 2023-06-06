---
title: Aspose::Words::CompositeNode::RemoveChild method
linktitle: RemoveChild
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::RemoveChild method. Removes the specified child node in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words/compositenode/removechild/
---
## CompositeNode::RemoveChild method


Removes the specified child node.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::RemoveChild(const System::SharedPtr<Aspose::Words::Node> &oldChild)
```


| Parameter | Type | Description |
| --- | --- | --- |
| oldChild | const System::SharedPtr\<Aspose::Words::Node\>\& | The node to remove. |

### ReturnValue

The removed node.
## Remarks


The parent of *oldChild* is set to **null** after the node is removed.

## Examples



Shows how to use of methods of [Node](../../node/) and [CompositeNode](../) to remove a section before the last section in the document. 
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

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

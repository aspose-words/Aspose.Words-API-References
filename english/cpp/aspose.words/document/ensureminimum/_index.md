---
title: Aspose::Words::Document::EnsureMinimum method
linktitle: EnsureMinimum
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::EnsureMinimum method. If the document contains no sections, creates one section with one paragraph in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words/document/ensureminimum/
---
## Document::EnsureMinimum method


If the document contains no sections, creates one section with one paragraph.

```cpp
void Aspose::Words::Document::EnsureMinimum()
```


## Examples



Shows how to ensure that a document contains the minimal set of nodes required for editing its contents. 
```cpp
// A newly created document contains one child Section, which includes one child Body and one child Paragraph.
// We can edit the document body's contents by adding nodes such as Runs or inline Shapes to that paragraph.
auto doc = MakeObject<Document>();
SharedPtr<NodeCollection> nodes = doc->GetChildNodes(NodeType::Any, true);

ASSERT_EQ(NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASPOSE_ASSERT_EQ(doc, nodes->idx_get(0)->get_ParentNode());

ASSERT_EQ(NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(0), nodes->idx_get(1)->get_ParentNode());

ASSERT_EQ(NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(1), nodes->idx_get(2)->get_ParentNode());

// This is the minimal set of nodes that we need to be able to edit the document.
// We will no longer be able to edit the document if we remove any of them.
doc->RemoveAllChildren();

ASSERT_EQ(0, doc->GetChildNodes(NodeType::Any, true)->get_Count());

// Call this method to make sure that the document has at least those three nodes so we can edit it again.
doc->EnsureMinimum();

ASSERT_EQ(NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASSERT_EQ(NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASSERT_EQ(NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());

(System::ExplicitCast<Paragraph>(nodes->idx_get(2)))->get_Runs()->Add(MakeObject<Run>(doc, u"Hello world!"));
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

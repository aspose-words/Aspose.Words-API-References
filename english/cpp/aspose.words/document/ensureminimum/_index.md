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
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(NodeType::Any, true);

ASSERT_EQ(nodes->idx_get(0)->get_NodeType(), NodeType::Section);
ASPOSE_ASSERT_EQ(nodes->idx_get(0)->get_ParentNode(), doc);

ASSERT_EQ(nodes->idx_get(1)->get_NodeType(), NodeType::Body);
ASPOSE_ASSERT_EQ(nodes->idx_get(1)->get_ParentNode(), nodes->idx_get(0));

ASSERT_EQ(nodes->idx_get(2)->get_NodeType(), NodeType::Paragraph);
ASPOSE_ASSERT_EQ(nodes->idx_get(2)->get_ParentNode(), nodes->idx_get(1));

// This is the minimal set of nodes that we need to be able to edit the document.
// We will no longer be able to edit the document if we remove any of them.
doc->RemoveAllChildren();

ASSERT_EQ(doc->GetChildNodes(NodeType::Any, true)->get_Count(), 0);

// Call this method to make sure that the document has at least those three nodes so we can edit it again.
doc->EnsureMinimum();

ASSERT_EQ(nodes->idx_get(0)->get_NodeType(), NodeType::Section);
ASSERT_EQ(nodes->idx_get(1)->get_NodeType(), NodeType::Body);
ASSERT_EQ(nodes->idx_get(2)->get_NodeType(), NodeType::Paragraph);

(System::ExplicitCast<Aspose::Words::Paragraph>(nodes->idx_get(2)))->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```
## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

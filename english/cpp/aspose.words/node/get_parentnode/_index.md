---
title: get_ParentNode
second_title: Aspose.Words for C++ API Reference
description: Gets the immediate parent of this node.
type: docs
weight: 92
url: /cpp/aspose.words/node/get_parentnode/
---
## Node::get_ParentNode method


Gets the immediate parent of this node.

```cpp
System::SharedPtr<Aspose::Words::CompositeNode> Aspose::Words::Node::get_ParentNode()
```

## Remarks


If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is null.

## Examples



Shows how to access a node's parent node. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Append a child Run node to the document's first paragraph.
auto run = MakeObject<Run>(doc, u"Hello world!");
para->AppendChild(run);

// The paragraph is the parent node of the run node. We can trace this lineage
// all the way to the document node, which is the root of the document's node tree.
ASPOSE_ASSERT_EQ(para, run->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection(), doc->get_FirstSection()->get_Body()->get_ParentNode());
ASPOSE_ASSERT_EQ(doc, doc->get_FirstSection()->get_ParentNode());
```


Shows how to create a node and set its owning document. 
```cpp
auto doc = MakeObject<Document>();
auto para = MakeObject<Paragraph>(doc);
para->AppendChild(MakeObject<Run>(doc, u"Hello world!"));

// We have not yet appended this paragraph as a child to any composite node.
ASSERT_TRUE(para->get_ParentNode() == nullptr);

// If a node is an appropriate child node type of another composite node,
// we can attach it as a child only if both nodes have the same owner document.
// The owner document is the document we passed to the node's constructor.
// We have not attached this paragraph to the document, so the document does not contain its text.
ASPOSE_ASSERT_EQ(para->get_Document(), doc);
ASSERT_EQ(String::Empty, doc->GetText().Trim());

// Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
para->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));

// Add this node to the document, and then verify its contents.
doc->get_FirstSection()->get_Body()->AppendChild(para);

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## See Also

* Class [CompositeNode](../../compositenode/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)

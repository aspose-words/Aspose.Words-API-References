---
title: Add
second_title: Aspose.Words for C++ API Reference
description: Adds a node to the end of the collection.
type: docs
weight: 14
url: /cpp/aspose.words/nodecollection/add/
---
## NodeCollection::Add method


Adds a node to the end of the collection.

```cpp
void Aspose::Words::NodeCollection::Add(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Type | Description |
| --- | --- | --- |
| node | const System::SharedPtr\<Aspose::Words::Node\>\& | The node to be added to the end of the collection. |
## Remarks


The node is inserted as a child into the node object from which the collection was created.

If the node being inserted was created from another document, you should use [ImportNode()](../) to import the node to the current document. The imported node can then be inserted into the current document.

## Examples



Shows how to prepare a new section node for editing. 
```cpp
auto doc = MakeObject<Document>();

// A blank document comes with a section, which has a body, which in turn has a paragraph.
// We can add contents to this document by adding elements such as text runs, shapes, or tables to that paragraph.
ASSERT_EQ(NodeType::Section, doc->GetChild(NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(NodeType::Any, 0, true)->get_NodeType());

// If we add a new section like this, it will not have a body, or any other child nodes.
doc->get_Sections()->Add(MakeObject<Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(NodeType::Any, true)->get_Count());

// Run the "EnsureMinimum" method to add a body and a paragraph to this section to begin editing it.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild(MakeObject<Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## See Also

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)

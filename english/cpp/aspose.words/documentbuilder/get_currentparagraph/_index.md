---
title: Aspose::Words::DocumentBuilder::get_CurrentParagraph method
linktitle: get_CurrentParagraph
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::get_CurrentParagraph method. Gets the paragraph that is currently selected in this DocumentBuilder in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/documentbuilder/get_currentparagraph/
---
## DocumentBuilder::get_CurrentParagraph method


Gets the paragraph that is currently selected in this [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::DocumentBuilder::get_CurrentParagraph()
```


## Examples



Shows how to move a document builder's cursor to different nodes in a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
// and a bookmark end node.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

SharedPtr<NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ChildNodes();

ASSERT_EQ(NodeType::BookmarkStart, firstParagraphNodes->idx_get(0)->get_NodeType());
ASSERT_EQ(NodeType::Run, firstParagraphNodes->idx_get(1)->get_NodeType());
ASSERT_EQ(u"Bookmark contents.", firstParagraphNodes->idx_get(1)->GetText().Trim());
ASSERT_EQ(NodeType::BookmarkEnd, firstParagraphNodes->idx_get(2)->get_NodeType());

// The document builder's cursor is always ahead of the node that we last added with it.
// If the builder's cursor is at the end of the document, its current node will be null.
// The previous node is the bookmark end node that we last added.
// Adding new nodes with the builder will append them to the last node.
ASSERT_TRUE(builder->get_CurrentNode() == nullptr);

// If we wish to edit a different part of the document with the builder,
// we will need to bring its cursor to the node we wish to edit.
builder->MoveToBookmark(u"MyBookmark");

// Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
ASPOSE_ASSERT_EQ(firstParagraphNodes->idx_get(1), builder->get_CurrentNode());

// We can also move the cursor to an individual node like this.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(NodeType::Any, false)->idx_get(0));

ASSERT_EQ(NodeType::BookmarkStart, builder->get_CurrentNode()->get_NodeType());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), builder->get_CurrentParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// We can use specific methods to move to the start/end of a document.
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```

## See Also

* Class [Paragraph](../../paragraph/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

---
title: Aspose::Words::DocumentBuilder::get_IsAtEndOfParagraph method
linktitle: get_IsAtEndOfParagraph
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::get_IsAtEndOfParagraph method. Returns true if the cursor is at the end of the current paragraph in C++.'
type: docs
weight: 83000
url: /cpp/aspose.words/documentbuilder/get_isatendofparagraph/
---
## DocumentBuilder::get_IsAtEndOfParagraph method


Returns **true** if the cursor is at the end of the current paragraph.

```cpp
bool Aspose::Words::DocumentBuilder::get_IsAtEndOfParagraph()
```

## Examples


Shows how to move a document builder's cursor to different nodes in a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
// and a bookmark end node.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

System::SharedPtr<Aspose::Words::NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(NodeType::Any, false);

ASSERT_EQ(firstParagraphNodes->idx_get(0)->get_NodeType(), NodeType::BookmarkStart);
ASSERT_EQ(firstParagraphNodes->idx_get(1)->get_NodeType(), NodeType::Run);
ASSERT_EQ(firstParagraphNodes->idx_get(1)->GetText().Trim(), u"Bookmark contents.");
ASSERT_EQ(firstParagraphNodes->idx_get(2)->get_NodeType(), NodeType::BookmarkEnd);

// The document builder's cursor is always ahead of the node that we last added with it.
// If the builder's cursor is at the end of the document, its current node will be null.
// The previous node is the bookmark end node that we last added.
// Adding new nodes with the builder will append them to the last node.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// If we wish to edit a different part of the document with the builder,
// we will need to bring its cursor to the node we wish to edit.
builder->MoveToBookmark(u"MyBookmark");

// Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
ASPOSE_ASSERT_EQ(builder->get_CurrentNode(), firstParagraphNodes->idx_get(1));

// We can also move the cursor to an individual node like this.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(NodeType::Any, false)->idx_get(0));

ASSERT_EQ(builder->get_CurrentNode()->get_NodeType(), NodeType::BookmarkStart);
ASPOSE_ASSERT_EQ(builder->get_CurrentParagraph(), doc->get_FirstSection()->get_Body()->get_FirstParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// We can use specific methods to move to the start/end of a document.
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```
## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

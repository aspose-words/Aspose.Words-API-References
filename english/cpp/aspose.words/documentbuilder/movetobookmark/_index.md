---
title: MoveToBookmark
second_title: Aspose.Words for C++ API Reference
description: Moves the cursor to a bookmark.
type: docs
weight: 664
url: /cpp/aspose.words/documentbuilder/movetobookmark/
---
## DocumentBuilder::MoveToBookmark(const System::String\&) method


Moves the cursor to a bookmark.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | The name of the bookmark to move the cursor to. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Remarks


Moves the cursor to a position just after the start of the bookmark with the specified name.

The comparison is not case-sensitive. If the bookmark was not found, **false** is returned and the cursor is not moved.

Inserting new text does not replace existing text of the bookmark.

Note that some bookmarks in the document are assigned to form fields. Moving to such a bookmark and inserting text there inserts the text into the form field code. Although this will not invalidate the form field, the inserted text will not be visible because it becomes part of the field code.

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

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::MoveToBookmark(const System::String\&, bool, bool) method


Moves the cursor to a bookmark with greater precision.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName, bool isStart, bool isAfter)
```


| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | The name of the bookmark to move the cursor to. |
| isStart | bool | When **true**, moves the cursor to the beginning of the bookmark. When **false**, moves the cursor to the end of the bookmark. |
| isAfter | bool | When **true**, moves the cursor to be after the bookmark start or end position. When **false**, moves the cursor to be before the bookmark start or end position. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Remarks


Moves the cursor to a position before or after the bookmark start or end.

If desired position is not at inline level, moves to the next paragraph.

The comparison is not case-sensitive. If the bookmark was not found, **false** is returned and the cursor is not moved.

## Examples



Shows how to move a document builder's node insertion point cursor to a bookmark. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A valid bookmark consists of a BookmarkStart node, a BookmarkEnd node with a
// matching bookmark name somewhere afterward, and contents enclosed by those nodes.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world! ");
builder->EndBookmark(u"MyBookmark");

// There are 4 ways of moving a document builder's cursor to a bookmark.
// If we are between the BookmarkStart and BookmarkEnd nodes, the cursor will be inside the bookmark.
// This means that any text added by the builder will become a part of the bookmark.
// 1 -  Outside of the bookmark, in front of the BookmarkStart node:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, false));
builder->Write(u"1. ");

ASSERT_EQ(u"Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. Hello world!", doc->GetText().Trim());

// 2 -  Inside the bookmark, right after the BookmarkStart node:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, true));
builder->Write(u"2. ");

ASSERT_EQ(u"2. Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world!", doc->GetText().Trim());

// 2 -  Inside the bookmark, right in front of the BookmarkEnd node:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, false));
builder->Write(u"3. ");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3.", doc->GetText().Trim());

// 4 -  Outside of the bookmark, after the BookmarkEnd node:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, true));
builder->Write(u"4.");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3. 4.", doc->GetText().Trim());
```

## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)

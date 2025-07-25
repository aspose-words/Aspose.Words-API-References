---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: Aspose.Words for .NET
description: Effortlessly navigate your documents with the DocumentBuilder MoveToBookmark method, instantly positioning the cursor at any bookmark for enhanced editing.
type: docs
weight: 530
url: /net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

Moves the cursor to a bookmark.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | String | The name of the bookmark to move the cursor to. |

### Return Value

`true` if the bookmark was found; `false` otherwise.

## Remarks

Moves the cursor to a position just after the start of the bookmark with the specified name.

The comparison is not case-sensitive. If the bookmark was not found, `false` is returned and the cursor is not moved.

Inserting new text does not replace existing text of the bookmark.

Note that some bookmarks in the document are assigned to form fields. Moving to such a bookmark and inserting text there inserts the text into the form field code. Although this will not invalidate the form field, the inserted text will not be visible because it becomes part of the field code.

## Examples

Shows how to move a document builder's cursor to different nodes in a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
// and a bookmark end node.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.That(firstParagraphNodes[0].NodeType, Is.EqualTo(NodeType.BookmarkStart));
Assert.That(firstParagraphNodes[1].NodeType, Is.EqualTo(NodeType.Run));
Assert.That(firstParagraphNodes[1].GetText().Trim(), Is.EqualTo("Bookmark contents."));
Assert.That(firstParagraphNodes[2].NodeType, Is.EqualTo(NodeType.BookmarkEnd));

// The document builder's cursor is always ahead of the node that we last added with it.
// If the builder's cursor is at the end of the document, its current node will be null.
// The previous node is the bookmark end node that we last added.
// Adding new nodes with the builder will append them to the last node.
Assert.That(builder.CurrentNode, Is.Null);

// If we wish to edit a different part of the document with the builder,
// we will need to bring its cursor to the node we wish to edit.
builder.MoveToBookmark("MyBookmark");

// Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
Assert.That(builder.CurrentNode, Is.EqualTo(firstParagraphNodes[1]));

// We can also move the cursor to an individual node like this.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.That(builder.CurrentNode.NodeType, Is.EqualTo(NodeType.BookmarkStart));
Assert.That(builder.CurrentParagraph, Is.EqualTo(doc.FirstSection.Body.FirstParagraph));
Assert.That(builder.IsAtStartOfParagraph, Is.True);

// We can use specific methods to move to the start/end of a document.
builder.MoveToDocumentEnd();

Assert.That(builder.IsAtEndOfParagraph, Is.True);

builder.MoveToDocumentStart();

Assert.That(builder.IsAtStartOfParagraph, Is.True);
```

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## MoveToBookmark(*string, bool, bool*) {#movetobookmark_1}

Moves the cursor to a bookmark with greater precision.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | String | The name of the bookmark to move the cursor to. |
| isStart | Boolean | When `true`, moves the cursor to the beginning of the bookmark. When `false`, moves the cursor to the end of the bookmark. |
| isAfter | Boolean | When `true`, moves the cursor to be after the bookmark start or end position. When `false`, moves the cursor to be before the bookmark start or end position. |

### Return Value

`true` if the bookmark was found; `false` otherwise.

## Remarks

Moves the cursor to a position before or after the bookmark start or end.

If desired position is not at inline level, moves to the next paragraph.

The comparison is not case-sensitive. If the bookmark was not found, `false` is returned and the cursor is not moved.

## Examples

Shows how to move a document builder's node insertion point cursor to a bookmark.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A valid bookmark consists of a BookmarkStart node, a BookmarkEnd node with a
// matching bookmark name somewhere afterward, and contents enclosed by those nodes.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// There are 4 ways of moving a document builder's cursor to a bookmark.
// If we are between the BookmarkStart and BookmarkEnd nodes, the cursor will be inside the bookmark.
// This means that any text added by the builder will become a part of the bookmark.
// 1 -  Outside of the bookmark, in front of the BookmarkStart node:
Assert.That(builder.MoveToBookmark("MyBookmark", true, false), Is.True);
builder.Write("1. ");

Assert.That(doc.Range.Bookmarks["MyBookmark"].Text, Is.EqualTo("Hello world! "));
Assert.That(doc.GetText().Trim(), Is.EqualTo("1. Hello world!"));

// 2 -  Inside the bookmark, right after the BookmarkStart node:
Assert.That(builder.MoveToBookmark("MyBookmark", true, true), Is.True);
builder.Write("2. ");

Assert.That(doc.Range.Bookmarks["MyBookmark"].Text, Is.EqualTo("2. Hello world! "));
Assert.That(doc.GetText().Trim(), Is.EqualTo("1. 2. Hello world!"));

// 2 -  Inside the bookmark, right in front of the BookmarkEnd node:
Assert.That(builder.MoveToBookmark("MyBookmark", false, false), Is.True);
builder.Write("3. ");

Assert.That(doc.Range.Bookmarks["MyBookmark"].Text, Is.EqualTo("2. Hello world! 3. "));
Assert.That(doc.GetText().Trim(), Is.EqualTo("1. 2. Hello world! 3."));

// 4 -  Outside of the bookmark, after the BookmarkEnd node:
Assert.That(builder.MoveToBookmark("MyBookmark", false, true), Is.True);
builder.Write("4.");

Assert.That(doc.Range.Bookmarks["MyBookmark"].Text, Is.EqualTo("2. Hello world! 3. "));
Assert.That(doc.GetText().Trim(), Is.EqualTo("1. 2. Hello world! 3. 4."));
```

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

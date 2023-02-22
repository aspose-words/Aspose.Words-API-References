---
title: EndColumnBookmark
second_title: Aspose.Words for .NET API Reference
description: DocumentBuilder method. Marks the current position in the document as a column bookmark end. The position must be in a table cell in C#.
type: docs
weight: 220
url: /net/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder.EndColumnBookmark method

Marks the current position in the document as a column bookmark end. The position must be in a table cell.

```csharp
public BookmarkEnd EndColumnBookmark(string bookmarkName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | String | Name of the bookmark. |

### Return Value

The bookmark end node that was just created.

## Remarks

A column bookmark covers one or more columns in a range of rows. To create a valid bookmark you need to call both [`StartColumnBookmark`](../startcolumnbookmark/) and `EndColumnBookmark` with the same *bookmarkName* parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

The actual position of the inserted [`BookmarkEnd`](../../bookmarkend/) node may differ from the current document builder position.

## Examples

Shows how to create a column bookmark.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// Cells 1,2,4,5 will be bookmarked.
builder.StartColumnBookmark("MyBookmark_1");
// Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
builder.StartColumnBookmark("MyBookmark_1");
builder.StartColumnBookmark("BadStartBookmark");
builder.Write("Cell 1");

builder.InsertCell();
builder.Write("Cell 2");

builder.InsertCell();
builder.Write("Cell 3");

builder.EndRow();

builder.InsertCell();
builder.Write("Cell 4");

builder.InsertCell();
builder.Write("Cell 5");
builder.EndColumnBookmark("MyBookmark_1");
builder.EndColumnBookmark("MyBookmark_1");

builder.InsertCell();
builder.Write("Cell 6");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "Bookmarks.CreateColumnBookmark.docx");
```

### See Also

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

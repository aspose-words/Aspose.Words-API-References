---
title: Aspose::Words::DocumentBuilder::StartColumnBookmark method
linktitle: StartColumnBookmark
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::StartColumnBookmark method. Marks the current position in the document as a column bookmark start. The position must be in a table cell in C++.'
type: docs
weight: 69000
url: /cpp/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder::StartColumnBookmark method


Marks the current position in the document as a column bookmark start. The position must be in a table cell.

```cpp
System::SharedPtr<Aspose::Words::BookmarkStart> Aspose::Words::DocumentBuilder::StartColumnBookmark(const System::String &bookmarkName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | Name of the bookmark. |

### ReturnValue

The bookmark start node that was just created.
## Remarks


A column bookmark covers one or more columns in a range of rows. To create a valid bookmark you need to call both [StartColumnBookmark()](../) and [EndColumnBookmark()](../) with the same *bookmarkName* parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

The actual position of the inserted [BookmarkStart](../../bookmarkstart/) node may differ from the current document builder position.

## Examples



Shows how to create a column bookmark. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->StartTable();

builder->InsertCell();
// Cells 1,2,4,5 will be bookmarked.
builder->StartColumnBookmark(u"MyBookmark_1");
// Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
builder->StartColumnBookmark(u"MyBookmark_1");
builder->StartColumnBookmark(u"BadStartBookmark");
builder->Write(u"Cell 1");

builder->InsertCell();
builder->Write(u"Cell 2");

builder->InsertCell();
builder->Write(u"Cell 3");

builder->EndRow();

builder->InsertCell();
builder->Write(u"Cell 4");

builder->InsertCell();
builder->Write(u"Cell 5");
builder->EndColumnBookmark(u"MyBookmark_1");
builder->EndColumnBookmark(u"MyBookmark_1");

builder->InsertCell();
builder->Write(u"Cell 6");

builder->EndRow();
builder->EndTable();

doc->Save(ArtifactsDir + u"Bookmarks.CreateColumnBookmark.docx");
```

## See Also

* Class [BookmarkStart](../../bookmarkstart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

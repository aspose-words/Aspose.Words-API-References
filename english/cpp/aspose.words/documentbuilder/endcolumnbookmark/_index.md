---
title: Aspose::Words::DocumentBuilder::EndColumnBookmark method
linktitle: EndColumnBookmark
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::EndColumnBookmark method. Marks the current position in the document as a column bookmark end. The position must be in a table cell in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder::EndColumnBookmark method


Marks the current position in the document as a column bookmark end. The position must be in a table cell.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndColumnBookmark(const System::String &bookmarkName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | Name of the bookmark. |

### ReturnValue

The bookmark end node that was just created.
## Remarks


A column bookmark covers one or more columns in a range of rows. To create a valid bookmark you need to call both [StartColumnBookmark()](../) and [EndColumnBookmark()](../) with the same *bookmarkName* parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

The actual position of the inserted [BookmarkEnd](../../bookmarkend/) node may differ from the current document builder position.

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

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

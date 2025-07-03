---
title: Aspose::Words::DocumentBuilder::EndBookmark method
linktitle: EndBookmark
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::EndBookmark method. Marks the current position in the document as a bookmark end in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder::EndBookmark method


Marks the current position in the document as a bookmark end.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndBookmark(const System::String &bookmarkName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | Name of the bookmark. |

### ReturnValue

The bookmark end node that was just created.
## Remarks


Bookmarks in a document can overlap and span any range. To create a valid bookmark you need to call both [StartBookmark()](../) and [EndBookmark()](../) with the same *bookmarkName* parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

## Examples



Shows how create a bookmark. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A valid bookmark needs to have document body text enclosed by
// BookmarkStart and BookmarkEnd nodes created with a matching bookmark name.
builder->StartBookmark(u"MyBookmark");
builder->Writeln(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

ASSERT_EQ(1, doc->get_Range()->get_Bookmarks()->get_Count());
ASSERT_EQ(u"MyBookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());
ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Text().Trim());
```


Shows how to insert a hyperlink which references a local bookmark. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Insert a HYPERLINK field that links to the bookmark. We can pass field switches
// to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## See Also

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

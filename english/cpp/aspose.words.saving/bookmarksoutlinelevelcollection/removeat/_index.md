---
title: Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt method
linktitle: RemoveAt
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt method. Removes a bookmark at the specified index in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words.saving/bookmarksoutlinelevelcollection/removeat/
---
## BookmarksOutlineLevelCollection::RemoveAt method


Removes a bookmark at the specified index.

```cpp
void Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | The zero based index. |

## Examples



Shows how to set outline levels for bookmarks. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a bookmark with another bookmark nested inside it.
builder->StartBookmark(u"Bookmark 1");
builder->Writeln(u"Text inside Bookmark 1.");

builder->StartBookmark(u"Bookmark 2");
builder->Writeln(u"Text inside Bookmark 1 and 2.");
builder->EndBookmark(u"Bookmark 2");

builder->Writeln(u"Text inside Bookmark 1.");
builder->EndBookmark(u"Bookmark 1");

// Insert another bookmark.
builder->StartBookmark(u"Bookmark 3");
builder->Writeln(u"Text inside Bookmark 3.");
builder->EndBookmark(u"Bookmark 3");

// When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
// Bookmarks can also have numeric values for outline levels,
// enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
auto pdfSaveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
System::SharedPtr<Aspose::Words::Saving::BookmarksOutlineLevelCollection> outlineLevels = pdfSaveOptions->get_OutlineOptions()->get_BookmarksOutlineLevels();

outlineLevels->Add(u"Bookmark 1", 1);
outlineLevels->Add(u"Bookmark 2", 2);
outlineLevels->Add(u"Bookmark 3", 3);

ASSERT_EQ(3, outlineLevels->get_Count());
ASSERT_TRUE(outlineLevels->Contains(u"Bookmark 1"));
ASSERT_EQ(1, outlineLevels->idx_get(0));
ASSERT_EQ(2, outlineLevels->idx_get(u"Bookmark 2"));
ASSERT_EQ(2, outlineLevels->IndexOfKey(u"Bookmark 3"));

// We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
outlineLevels->RemoveAt(2);
outlineLevels->Remove(u"Bookmark 2");

// There are nine outline levels. Their numbering will be optimized during the save operation.
// In this case, levels "5" and "9" will become "2" and "3".
outlineLevels->Add(u"Bookmark 2", 5);
outlineLevels->Add(u"Bookmark 3", 9);

doc->Save(get_ArtifactsDir() + u"BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Emptying this collection will preserve the bookmarks and put them all on the same outline level.
outlineLevels->Clear();
```

## See Also

* Class [BookmarksOutlineLevelCollection](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

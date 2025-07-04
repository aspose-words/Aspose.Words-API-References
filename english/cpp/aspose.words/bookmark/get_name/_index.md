---
title: Aspose::Words::Bookmark::get_Name method
linktitle: get_Name
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Bookmark::get_Name method. Gets or sets the name of the bookmark in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/bookmark/get_name/
---
## Bookmark::get_Name method


Gets or sets the name of the bookmark.

```cpp
System::String Aspose::Words::Bookmark::get_Name()
```


## Examples



Shows how to insert a bookmark. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A valid bookmark has a name, a BookmarkStart, and a BookmarkEnd node.
// Any whitespace in the names of bookmarks will be converted to underscores if we open the saved document with Microsoft Word.
// If we highlight the bookmark's name in Microsoft Word via Insert -> Links -> Bookmark, and press "Go To",
// the cursor will jump to the text enclosed between the BookmarkStart and BookmarkEnd nodes.
builder->StartBookmark(u"My Bookmark");
builder->Write(u"Contents of MyBookmark.");
builder->EndBookmark(u"My Bookmark");

// Bookmarks are stored in this collection.
ASSERT_EQ(u"My Bookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());

doc->Save(get_ArtifactsDir() + u"Bookmarks.Insert.docx");
```

## See Also

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

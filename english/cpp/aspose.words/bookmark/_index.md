---
title: Aspose::Words::Bookmark class
linktitle: Bookmark
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Bookmark class. Represents a single bookmark. To learn more, visit the  documentation article in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/bookmark/
---
## Bookmark class


Represents a single bookmark. To learn more, visit the [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) documentation article.

```cpp
class Bookmark : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_BookmarkEnd](./get_bookmarkend/)() | Gets the node that represents the end of the bookmark. |
| [get_BookmarkStart](./get_bookmarkstart/)() const | Gets the node that represents the start of the bookmark. |
| [get_FirstColumn](./get_firstcolumn/)() | Gets the zero-based index of the first column of the table column range associated with the bookmark. |
| [get_IsColumn](./get_iscolumn/)() | Returns **true** if this bookmark is a table column bookmark. |
| [get_LastColumn](./get_lastcolumn/)() | Gets the zero-based index of the last column of the table column range associated with the bookmark. |
| [get_Name](./get_name/)() | Gets or sets the name of the bookmark. |
| [get_Text](./get_text/)() | Gets the text enclosed in the bookmark. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Removes the bookmark from the document. Does not remove text inside the bookmark. |
| [set_Name](./set_name/)(const System::String\&) | Setter for [Aspose::Words::Bookmark::get_Name](./get_name/). |
| [set_Text](./set_text/)(const System::String\&) | Sets the text enclosed in the bookmark. |
| static [Type](./type/)() |  |
## Remarks


[Bookmark](./) is a "facade" object that encapsulates two nodes [BookmarkStart](./get_bookmarkstart/) and [BookmarkEnd](./get_bookmarkend/) in a document tree and allows to work with a bookmark as a single object. 
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

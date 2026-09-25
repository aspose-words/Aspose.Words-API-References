---
title: Aspose::Words::Bookmark::get_IsColumn method
linktitle: get_IsColumn
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Bookmark::get_IsColumn method. Returns true if this bookmark is a table column bookmark in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/bookmark/get_iscolumn/
---
## Bookmark::get_IsColumn method


Returns **true** if this bookmark is a table column bookmark.

```cpp
bool Aspose::Words::Bookmark::get_IsColumn()
```


## Examples



Shows how to get information about table column bookmarks. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Table column bookmarks.doc"));

for (auto&& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // If a bookmark encloses columns of a table, it is a table column bookmark, and its IsColumn flag set to true.
    System::Console::WriteLine(System::String::Format(u"Bookmark: {0}{1}", bookmark->get_Name(), bookmark->get_IsColumn() ? System::String(u" (Column)") : System::String(u"")));
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Aspose::Words::Tables::Row>(bookmark->get_BookmarkStart()->GetAncestor(Aspose::Words::NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // Print the contents of the first and last columns enclosed by the bookmark.
            System::Console::WriteLine(row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(ControlChar::CellChar));
            System::Console::WriteLine(row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(ControlChar::CellChar));
        }
    }
}
```

## See Also

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

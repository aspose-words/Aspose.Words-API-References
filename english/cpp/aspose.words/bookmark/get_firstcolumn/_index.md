---
title: Aspose::Words::Bookmark::get_FirstColumn method
linktitle: get_FirstColumn
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Bookmark::get_FirstColumn method. Gets the zero-based index of the first column of the table column range associated with the bookmark in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/bookmark/get_firstcolumn/
---
## Bookmark::get_FirstColumn method


Gets the zero-based index of the first column of the table column range associated with the bookmark.

```cpp
int32_t Aspose::Words::Bookmark::get_FirstColumn()
```


## Examples



Shows how to get information about table column bookmarks. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table column bookmarks.doc");

for (auto&& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // If a bookmark encloses columns of a table, it is a table column bookmark, and its IsColumn flag set to true.
    std::cout << System::String::Format(u"Bookmark: {0}{1}", bookmark->get_Name(), (bookmark->get_IsColumn() ? System::String(u" (Column)") : System::String(u""))) << std::endl;
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Aspose::Words::Tables::Row>(bookmark->get_BookmarkStart()->GetAncestor(Aspose::Words::NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // Print the contents of the first and last columns enclosed by the bookmark.
            std::cout << row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
            std::cout << row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
        }
    }
}
```

## See Also

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

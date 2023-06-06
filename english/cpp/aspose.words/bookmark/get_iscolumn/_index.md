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
auto doc = MakeObject<Document>(MyDir + u"Table column bookmarks.doc");

for (const auto& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // If a bookmark encloses columns of a table, it is a table column bookmark, and its IsColumn flag set to true.
    std::cout << "Bookmark: " << bookmark->get_Name() << (bookmark->get_IsColumn() ? String(u" (Column)") : String(u"")) << std::endl;
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Row>(bookmark->get_BookmarkStart()->GetAncestor(NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // Print the contents of the first and last columns enclosed by the bookmark.
            std::cout << row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(MakeArray<char16_t>({ControlChar::CellChar}))
                      << std::endl;
            std::cout << row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(MakeArray<char16_t>({ControlChar::CellChar}))
                      << std::endl;
        }
    }
}
```

## See Also

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

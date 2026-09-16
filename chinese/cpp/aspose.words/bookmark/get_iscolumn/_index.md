---
title: "Aspose::Words::Bookmark::get_IsColumn 方法"
linktitle: "get_IsColumn"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Bookmark::get_IsColumn 方法。若此书签是表列书签，则返回 true（C++）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/bookmark/get_iscolumn/
---
## Bookmark::get_IsColumn method


如果此书签是表列书签，则返回 **true**。

```cpp
bool Aspose::Words::Bookmark::get_IsColumn()
```


## 示例



展示如何获取表列书签的信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table column bookmarks.doc");

for (auto&& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // 如果书签包含表的列，则它是表列书签，并且其 IsColumn 标志被设置为 true。
    std::cout << System::String::Format(u"Bookmark: {0}{1}", bookmark->get_Name(), (bookmark->get_IsColumn() ? System::String(u" (Column)") : System::String(u""))) << std::endl;
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Aspose::Words::Tables::Row>(bookmark->get_BookmarkStart()->GetAncestor(Aspose::Words::NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // 打印书签所包含的第一列和最后一列的内容。
            std::cout << row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
            std::cout << row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
        }
    }
}
```

## 另见

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

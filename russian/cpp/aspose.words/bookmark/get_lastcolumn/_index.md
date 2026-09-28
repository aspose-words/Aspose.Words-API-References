---
title: "Aspose::Words::Bookmark::get_LastColumn метод"
linktitle: "get_LastColumn"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Bookmark::get_LastColumn метод. Получает индекс последнего столбца диапазона столбцов таблицы, связанного с закладкой, нумерация начинается с нуля, в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/bookmark/get_lastcolumn/
---
## Bookmark::get_LastColumn method


Получает нулевой индекс последней колонки диапазона столбцов таблицы, связанного с закладкой.

```cpp
int32_t Aspose::Words::Bookmark::get_LastColumn()
```


## Примеры



Показывает, как получить информацию о закладках столбцов таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table column bookmarks.doc");

for (auto&& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // Если закладка охватывает столбцы таблицы, это закладка столбца таблицы, и её флаг IsColumn установлен в true.
    std::cout << System::String::Format(u"Bookmark: {0}{1}", bookmark->get_Name(), (bookmark->get_IsColumn() ? System::String(u" (Column)") : System::String(u""))) << std::endl;
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Aspose::Words::Tables::Row>(bookmark->get_BookmarkStart()->GetAncestor(Aspose::Words::NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // Выведите содержимое первого и последнего столбцов, охваченных закладкой.
            std::cout << row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
            std::cout << row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
        }
    }
}
```

## См. также

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

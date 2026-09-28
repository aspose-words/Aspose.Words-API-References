---
title: "Метод Aspose::Words::Tables::Cell::get_NextCell"
linktitle: "get_NextCell"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Tables::Cell::get_NextCell. Получает следующую ячейку Cell в C++."
type: docs
weight: 9500
url: /ru/cpp/aspose.words.tables/cell/get_nextcell/
---
## Cell::get_NextCell method


Получает следующий узел [Cell](../).

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::Tables::Cell::get_NextCell()
```


## Примеры



Показывает, как перечислять все ячейки таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Перечислите все ячейки таблицы.
for (System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_FirstRow(); row != nullptr; row = row->get_NextRow())
{
    for (System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_FirstCell(); cell != nullptr; cell = cell->get_NextCell())
    {
        std::cout << cell->GetText() << std::endl;
    }
}
```

## См. также

* Class [Cell](../)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

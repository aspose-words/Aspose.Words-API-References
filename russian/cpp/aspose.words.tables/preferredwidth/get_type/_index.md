---
title: "Aspose::Words::Tables::PreferredWidth::get_Type метод"
linktitle: "get_Type"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::PreferredWidth::get_Type метод. Получает единицу измерения, используемую для этого значения предпочтительной ширины в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.tables/preferredwidth/get_type/
---
## PreferredWidth::get_Type method


Получает единицу измерения, используемую для этого значения предпочтительной ширины.

```cpp
Aspose::Words::Tables::PreferredWidthType Aspose::Words::Tables::PreferredWidth::get_Type() const
```


## Примеры



Показывает, как проверить тип и значение предпочтительной ширины ячейки таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## См. также

* Enum [PreferredWidthType](../../preferredwidthtype/)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

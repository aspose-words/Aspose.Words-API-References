---
title: "Aspose::Words::Tables::PreferredWidth::get_Value метод"
linktitle: "get_Value"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::PreferredWidth::get_Value метод. Получает значение предпочтительной ширины. Единица измерения указывается в свойстве Type в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.tables/preferredwidth/get_value/
---
## PreferredWidth::get_Value method


Получает значение предпочтительной ширины. Единица измерения указывается в свойстве [Type](../get_type/).

```cpp
double Aspose::Words::Tables::PreferredWidth::get_Value() const
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

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

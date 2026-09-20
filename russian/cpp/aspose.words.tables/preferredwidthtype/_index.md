---
title: "Aspose::Words::Tables::PreferredWidthType enum"
linktitle: "PreferredWidthType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::PreferredWidthType enum. Указывает единицу измерения предпочтительной ширины таблицы или ячейки в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enum


Указывает единицу измерения предпочтительной ширины таблицы или ячейки.

```cpp
enum class PreferredWidthType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Авто | 1 | Предпочтительная ширина не указана. Фактическая ширина таблицы или ячейки либо задаётся явно, либо будет определена автоматически алгоритмом компоновки таблицы при отображении, в зависимости от настройки автоматической подгонки таблицы. |
| Процент | 2 | Измерьте текущую ширину элемента, используя указанный процент. |
| Пункты | 3 | Измерьте текущую ширину элемента, используя указанное количество пунктов (1/72 дюйма). |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)

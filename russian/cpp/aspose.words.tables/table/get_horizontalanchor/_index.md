---
title: "Aspose::Words::Tables::Table::get_HorizontalAnchor метод"
linktitle: "get_HorizontalAnchor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::get_HorizontalAnchor метод. Получает базовый объект, от которого следует рассчитывать горизонтальное позиционирование плавающей таблицы. Значение по умолчанию — Column в C++."
type: docs
weight: 24000
url: /ru/cpp/aspose.words.tables/table/get_horizontalanchor/
---
## Table::get_HorizontalAnchor method


Получает базовый объект, от которого следует рассчитывать горизонтальное позиционирование плавающей таблицы. Значение по умолчанию — [Column](../../../aspose.words.drawing/relativehorizontalposition/).

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Tables::Table::get_HorizontalAnchor()
```


## Примеры



Показывает, как работать со свойствами плавающих таблиц.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == Aspose::Words::Tables::TextWrapping::Around)
{
    ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // Для свойства HorizontalAnchor в RelativeHorizontalPosition доступны только Margin, Page, Column.
    // Будет выброшено исключение ArgumentException для любых других значений.
    table->set_HorizontalAnchor(Aspose::Words::Drawing::RelativeHorizontalPosition::Column);

    // Для свойства VerticalAnchor в RelativeVerticalPosition доступны только Margin, Page, Paragraph.
    // Будет выброшено исключение ArgumentException для любых других значений.
    table->set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
}
```

## См. также

* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap метод"
linktitle: "get_AllowOverlap"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap метод. Получает или задает значение, указывающее, может ли эта форма перекрывать другие формы в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.drawing/shapebase/get_allowoverlap/
---
## ShapeBase::get_AllowOverlap method


Получает или задает значение, указывающее, может ли эта фигура перекрывать другие фигуры.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AllowOverlap()
```

## Примечания


Это свойство влияет на поведение формы в Microsoft Word. Aspose.Words игнорирует значение этого свойства.

Это свойство применимо только к формам верхнего уровня.

Значение по умолчанию — **true**.

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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

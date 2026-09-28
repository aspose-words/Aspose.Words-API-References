---
title: "Перечисление Aspose::Words::Drawing::GradientStyle"
linktitle: "GradientStyle"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Drawing::GradientStyle. Указывает стиль градиентной заливки в C++."
type: docs
weight: 24000
url: /ru/cpp/aspose.words.drawing/gradientstyle/
---
## GradientStyle enum


Указывает стиль градиентной заливки.

```cpp
enum class GradientStyle
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | -1 | Без градиента. |
| Горизонтальная | 1 | Градиент, проходящий горизонтально через объект. |
| Вертикальная | 2 | Градиент, проходящий вертикально вниз по объекту. |
| ДиагональВверх | 3 | Диагональный градиент, перемещающийся от нижнего угла к противоположному. |
| ДиагональВниз | 4 | Диагональный градиент, перемещающийся от верхнего угла к противоположному. |
| FromCorner | 5 | Градиент, идущий от одного угла к трем другим углам. |
| FromCenter | 6 | Градиент, исходящий из центра к углам. |


## Примеры



Показывает, как заполнить форму градиентами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Применить однокрасный градиент к форме с ForeColor градиентной заливки.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Применить двухцветный градиент к форме.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// Изменить BackColor градиентной заливки.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Обратите внимание, что изменяется "GradientAngle" для "GradientStyle.FromCorner/GradientStyle.FromCenter"
// Градиентная заливка не оказывает эффекта, она будет работать только для линейного градиента.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Используйте параметр совместимости, чтобы определить форму с помощью DML, если вы хотите получить "GradientStyle",
// "GradientVariant" и свойства "GradientAngle" после сохранения документа.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

---
title: "Aspose::Words::Drawing::Fill::get_GradientAngle метод"
linktitle: "get_GradientAngle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Fill::get_GradientAngle метод. Получает или задает угол градиентной заливки в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.drawing/fill/get_gradientangle/
---
## Fill::get_GradientAngle method


Получает или задает угол градиентной заливки.

```cpp
double Aspose::Words::Drawing::Fill::get_GradientAngle()
```


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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

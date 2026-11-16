---
title: Aspose::Words::Drawing::Fill::get_BaseForeColor method
linktitle: get_BaseForeColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::get_BaseForeColor method. Gets a Color object that represents the base foreground color for the fill without any modifiers in C++.'
type: docs
weight: 48000
url: /cpp/aspose.words.drawing/fill/get_baseforecolor/
---
## Fill::get_BaseForeColor method


Gets a Color object that represents the base foreground color for the fill without any modifiers.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Fill::get_BaseForeColor()
```

## Examples


Shows how to get foreground color without modifiers.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(ShapeType::Rectangle, static_cast<double>(100), static_cast<double>(40));
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
shape->get_Fill()->set_ForeTintAndShade(0.5);
shape->get_Stroke()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());
shape->get_Stroke()->get_Fill()->set_Transparency(0.5);

ASSERT_EQ(shape->get_Fill()->get_ForeColor().ToArgb(), System::Drawing::Color::FromArgb(255, 255, 188, 188).ToArgb());
ASSERT_EQ(shape->get_Fill()->get_BaseForeColor().ToArgb(), System::Drawing::Color::get_Red().ToArgb());

ASSERT_EQ(shape->get_Stroke()->get_ForeColor().ToArgb(), System::Drawing::Color::FromArgb(128, 0, 128, 0).ToArgb());
ASSERT_EQ(shape->get_Stroke()->get_BaseForeColor().ToArgb(), System::Drawing::Color::get_Green().ToArgb());

ASSERT_EQ(shape->get_Stroke()->get_Fill()->get_ForeColor().ToArgb(), System::Drawing::Color::get_Green().ToArgb());
ASSERT_EQ(shape->get_Stroke()->get_Fill()->get_BaseForeColor().ToArgb(), System::Drawing::Color::get_Green().ToArgb());
```
## See Also

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

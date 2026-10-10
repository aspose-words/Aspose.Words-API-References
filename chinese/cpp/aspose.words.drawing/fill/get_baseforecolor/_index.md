---
title: "Aspose::Words::Drawing::Fill::get_BaseForeColor 方法"
linktitle: "get_BaseForeColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Fill::get_BaseForeColor 方法。获取一个 Color 对象，表示填充的基础前景颜色（在 C++ 中），且不带任何修饰。"
type: docs
weight: 4500
url: /zh/cpp/aspose.words.drawing/fill/get_baseforecolor/
---
## Fill::get_BaseForeColor method


获取表示填充基础前景颜色（无任何修饰）的 Color 对象。

```cpp
System::Drawing::Color Aspose::Words::Drawing::Fill::get_BaseForeColor()
```


## 示例



展示如何获取不带修饰的前景颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
shape->get_Fill()->set_ForeTintAndShade(0.5);
shape->get_Stroke()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());
shape->get_Stroke()->get_Fill()->set_Transparency(0.5);

ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 188, 188).ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_BaseForeColor().ToArgb());

ASSERT_EQ(System::Drawing::Color::FromArgb(128, 0, 128, 0).ToArgb(), shape->get_Stroke()->get_ForeColor().ToArgb());
ASSERT_EQ(System::Drawing::Color::get_Green().ToArgb(), shape->get_Stroke()->get_BaseForeColor().ToArgb());

ASSERT_EQ(System::Drawing::Color::get_Green().ToArgb(), shape->get_Stroke()->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(System::Drawing::Color::get_Green().ToArgb(), shape->get_Stroke()->get_Fill()->get_BaseForeColor().ToArgb());
```

## 另见

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

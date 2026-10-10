---
title: "Aspose::Words::Drawing::Shape::get_StrokeColor 方法"
linktitle: "get_StrokeColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Shape::get_StrokeColor 方法。定义在 C++ 中描边的颜色。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words.drawing/shape/get_strokecolor/
---
## Shape::get_StrokeColor method


定义描边的颜色。

```cpp
System::Drawing::Color Aspose::Words::Drawing::Shape::get_StrokeColor()
```

## 备注


这是对 [Color](../../stroke/get_color/) 属性的快捷方式。

默认值是 **黑色**。

## 示例



展示如何使用纯色填充形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 写入一些文本，然后用浮动形状覆盖它。
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// 使用 \"StrokeColor\" 属性设置形状轮廓的颜色。
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// 使用 \"FillColor\" 属性设置形状内部区域的颜色。
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// “Opacity” 属性决定颜色在 0-1 量表上的透明度，
// 其中 1 表示完全不透明，0 表示不可见。
// 形状填充默认是完全不透明的，因此我们看不到该形状上方的文本。
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// 将形状填充颜色的透明度设置为较低的值，以便我们能看到其下方的文本。
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## 另见

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

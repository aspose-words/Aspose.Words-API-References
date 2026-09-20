---
title: "Aspose::Words::Drawing::Fill::get_Opacity 方法"
linktitle: "get_Opacity"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Fill::get_Opacity 方法。 获取或设置指定填充的不透明度程度，取值范围为 0.0（透明）到 1.0（不透明），在 C++ 中。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.drawing/fill/get_opacity/
---
## Fill::get_Opacity method


获取或设置指定填充的不透明度程度，取值范围为 0.0（透明）到 1.0（不透明）。

```cpp
double Aspose::Words::Drawing::Fill::get_Opacity()
```


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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

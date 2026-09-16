---
title: "Aspose::Words::Drawing::FlipOrientation 枚举"
linktitle: "FlipOrientation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::FlipOrientation 枚举。形状在 C++ 中方向的可能取值。"
type: docs
weight: 23000
url: /zh/cpp/aspose.words.drawing/fliporientation/
---
## FlipOrientation enum


形状方向的可能取值。

```cpp
enum class FlipOrientation
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 坐标未翻转。 |
| Horizontal | 1 | 沿 y 轴翻转，反转 x 坐标。 |
| Vertical | 2 | 沿 x 轴翻转，反转 y 坐标。 |
| Both | 3 | 同时沿 y 轴和 x 轴翻转。 |


## 示例



展示如何在轴上翻转形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入图像形状并保持其方向为默认状态。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::FlipOrientation::None, shape->get_FlipOrientation());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// 将 "FlipOrientation" 属性设置为 "FlipOrientation.Horizontal" 以在 y 轴上翻转第二个形状，
// 使其成为第一个形状的水平镜像。
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Horizontal);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// 将 "FlipOrientation" 属性设置为 "FlipOrientation.Horizontal" 以在 x 轴上翻转第三个形状，
// 使其成为第一个形状的垂直镜像。
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Vertical);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// 将 "FlipOrientation" 属性设置为 "FlipOrientation.Horizontal" 以在 x 轴和 y 轴上翻转第四个形状，
// 使其成为第一个形状的水平和垂直镜像。
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Both);

doc->Save(get_ArtifactsDir() + u"Shape.FlipShapeOrientation.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

---
title: "Aspose::Words::Drawing::ShapeBase::get_FlipOrientation method"
linktitle: "get_FlipOrientation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_FlipOrientation 方法。切换 C++ 中形状的方向。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words.drawing/shapebase/get_fliporientation/
---
## ShapeBase::get_FlipOrientation method


切换形状的方向。

```cpp
Aspose::Words::Drawing::FlipOrientation Aspose::Words::Drawing::ShapeBase::get_FlipOrientation()
```

## 备注


默认值是 [无](../../fliporientation/)。

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

* Enum [FlipOrientation](../../fliporientation/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints 方法"
linktitle: "get_BoundsInPoints"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints 方法。获取形状的包含块在点单位的位置和大小，相对于 C++ 中最上层形状的锚点。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.drawing/shapebase/get_boundsinpoints/
---
## ShapeBase::get_BoundsInPoints method


获取形状所在包含块的位置和大小（单位为点），相对于最上层形状的锚点。

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints()
```


## 示例



展示如何验证形状包含块的边界。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Line, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 50, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_StrokeColor(System::Drawing::Color::get_Orange());

// 即使该线本身在文档页面上占用的空间很小，
// 它占据一个矩形的包含块，我们可以使用 \"Bounds\" 属性来确定其大小。
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_Bounds());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

// 创建一个组形状，然后使用 \"Bounds\" 属性设置其包含块的大小。
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f));

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());

// 创建一个矩形，验证其边界块的大小，然后将其添加到组形状中。
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(700.0f, 700.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// 组形状的坐标平面原点位于其包含块的左上角，
// 以及右下角的 (1000, 1000) 的 x 和 y 坐标。
// 我们的组合形状大小为 250x250pt，因此在组合形状坐标平面上每 4pt
// 在文档正文的坐标平面上相当于 1pt。
// 我们插入的每个形状也会按 4 倍比例缩小尺寸。
// 形状的 \"BoundsInPoints\" 属性的更改将反映此情况。
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(175.0f, 275.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

// 插入一个形状并将其放置在组合形状所在容器块的边界之外。
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(1000);
shape->set_Top(1000);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// 组合形状在文档正文中的占位面积已增大，但容器块保持不变。
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(250.0f, 350.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->Save(get_ArtifactsDir() + u"Shape.Bounds.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

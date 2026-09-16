---
title: "Aspose::Words::Drawing::ShapeBase::get_Bounds 方法"
linktitle: "get_Bounds"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_Bounds 方法。获取或设置形状所在容器块的位置和大小（C++）。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.drawing/shapebase/get_bounds/
---
## ShapeBase::get_Bounds method


获取或设置形状所在包含块的位置和大小。

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_Bounds()
```

## 备注


设置时忽略宽高比锁定。

对于顶层形状，该值以点为单位，并相对于形状锚点。

对于组内的形状，该值使用父组的坐标空间和单位。

## 示例



展示如何创建和填充组形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建组形状。组形状可以显示一组子形状节点。
// 在 Microsoft Word 中，单击组形状的边界内或组形状的子形状之一将
// 选择该组内的所有其他子形状，并允许我们一次性缩放和移动所有形状。
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);

ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, group->get_WrapType());

// 创建一个 400pt x 400pt 的组形状，并将其放置在文档的浮动形状坐标原点。
group->set_Bounds(System::Drawing::RectangleF(0.0f, 0.0f, 400.0f, 400.0f));

// 将组的内部坐标平面大小设置为 500 x 500pt。
// 组的左上角的 x 和 y 坐标将为 (0, 0)，
// 右下角的 x 和 y 坐标将为 (500, 500)。
group->set_CoordSize(System::Drawing::Size(500, 500));

// 将组的左上角坐标设置为 (-250, -250)。
// 组的中心现在的 x 和 y 坐标值为 (0, 0)，
// 右下角将位于 (250, 250)。
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

// 创建一个矩形来显示此组形状的边界并将其添加到组中。
auto child1 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child1->set_Width(group->get_CoordSize().get_Width());
child1->set_Height(group->get_CoordSize().get_Height());
child1->set_Left(group->get_CoordOrigin().get_X());
child1->set_Top(group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child1);

// 一旦形状成为组形状的一部分，我们可以将其作为子节点访问并进行修改。
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::Dash);

// 创建一个小的红色星形并将其插入组中。
// 将形状与组的坐标原点对齐，我们已将其移动到中心。
auto child2 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Star);
child2->set_Width(20);
child2->set_Height(20);
child2->set_Left(-10);
child2->set_Top(-10);
child2->set_FillColor(System::Drawing::Color::get_Red());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child2);

// 插入一个矩形，然后在同一位置插入一个稍小的带有图像的矩形。
// 我们添加到组中的较新形状会覆盖较旧的形状。浅蓝色矩形将部分覆盖红色星形，
// 然后带有图像的形状会覆盖浅蓝色矩形，将其用作框架。
// 我们不能使用形状的 "ZOrder" 属性来操控它们在组形状中的排列。
auto child3 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child3->set_Width(250);
child3->set_Height(250);
child3->set_Left(-250);
child3->set_Top(-250);
child3->set_FillColor(System::Drawing::Color::get_LightBlue());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child3);

auto child4 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
child4->set_Width(200);
child4->set_Height(200);
child4->set_Left(-225);
child4->set_Top(-225);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child4);

(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 3, true)))->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// 在组形状中插入一个文本框。设置 "Left" 属性，使文本框的右边缘
// 接触组形状的右边界。设置 "Top" 属性，使文本框位于外部
// 组形状的边界，其顶部尺寸与组形状的底部边距对齐。
auto child5 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
child5->set_Width(200);
child5->set_Height(50);
child5->set_Left(group->get_CoordSize().get_Width() + group->get_CoordOrigin().get_X() - 200);
child5->set_Top(group->get_CoordSize().get_Height() + group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child5);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(group);
builder->MoveTo((System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 4, true)))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Shape.GroupShape.docx");
```


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

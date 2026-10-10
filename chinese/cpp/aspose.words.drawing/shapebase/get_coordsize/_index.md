---
title: "Aspose::Words::Drawing::ShapeBase::get_CoordSize 方法"
linktitle: "get_CoordSize"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_CoordSize 方法。此形状所在包含块内部坐标空间的宽度和高度（C++）。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.drawing/shapebase/get_coordsize/
---
## ShapeBase::get_CoordSize method


此形状的包含块内部坐标空间的宽度和高度。

```cpp
System::Drawing::Size Aspose::Words::Drawing::ShapeBase::get_CoordSize()
```

## 备注


默认值为 (1000, 1000)。

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


展示如何将形状坐标平面上的 x 和 y 坐标位置转换为父形状坐标平面上的位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 插入一个组形状，并将其放置在向下和向右各 100 点的位置
// 文档的 x 和 Y 坐标原点。
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 100.0f, 500.0f, 500.0f));

// 使用 "LocalToParent" 方法来确定组内部 x 和 y 坐标系中的 (0, 0)
// 位于其父形状坐标系的 (100, 100) 位置。组形状的父对象是文档本身。
ASPOSE_ASSERT_EQ(System::Drawing::PointF(100.0f, 100.0f), group->LocalToParent(System::Drawing::PointF(0.0f, 0.0f)));

// 默认情况下，形状的内部坐标平面的左上角位于 (0, 0)，
// 右下角位于 (1000, 1000)。由于其尺寸，我们的组形状覆盖了文档平面上 500pt x 500pt 的区域
// 在文档的平面中。这意味着文档坐标平面上移动 1pt 将会转换为
// 组形状坐标平面上移动 2pt。
ASPOSE_ASSERT_EQ(System::Drawing::PointF(150.0f, 150.0f), group->LocalToParent(System::Drawing::PointF(100.0f, 100.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(200.0f, 200.0f), group->LocalToParent(System::Drawing::PointF(200.0f, 200.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(250.0f, 250.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// 将组形状的 x 和 y 轴原点从左上角移动到中心。
// 这将进一步使组的内部坐标相对于文档坐标产生偏移。
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(375.0f, 375.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// 更改坐标平面的比例也会影响相对位置。
group->set_CoordSize(System::Drawing::Size(500, 500));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(650.0f, 650.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// 如果我们希望在此组中添加形状，并基于文档中的位置定义其位置，
// 我们需要首先确认组形状中的一个位置，以匹配文档的位置。
ASPOSE_ASSERT_EQ(System::Drawing::PointF(700.0f, 700.0f), group->LocalToParent(System::Drawing::PointF(350.0f, 350.0f)));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

doc->Save(get_ArtifactsDir() + u"Shape.LocalToParent.docx");
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

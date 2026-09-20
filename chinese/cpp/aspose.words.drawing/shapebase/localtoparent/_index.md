---
title: "Aspose::Words::Drawing::ShapeBase::LocalToParent 方法"
linktitle: "LocalToParent"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::LocalToParent 方法。将值从本地坐标空间转换为父形状的坐标空间（C++）。"
type: docs
weight: 61000
url: /zh/cpp/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase::LocalToParent method


将值从本地坐标空间转换为父形状的坐标空间。

```cpp
System::Drawing::PointF Aspose::Words::Drawing::ShapeBase::LocalToParent(System::Drawing::PointF value)
```


## 示例



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

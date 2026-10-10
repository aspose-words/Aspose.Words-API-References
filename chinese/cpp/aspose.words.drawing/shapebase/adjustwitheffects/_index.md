---
title: "Aspose::Words::Drawing::ShapeBase::AdjustWithEffects 方法"
linktitle: "AdjustWithEffects"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::AdjustWithEffects 方法。向源矩形添加效果范围的值并返回最终矩形，适用于 C++。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing/shapebase/adjustwitheffects/
---
## ShapeBase::AdjustWithEffects method


将效果范围的值添加到源矩形，并返回最终矩形。

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::AdjustWithEffects(System::Drawing::RectangleF source)
```


## 示例



展示如何检查形状的边界受形状效果的影响。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape shadow effect.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// 这两个形状在尺寸和形状类型上是相同的。
ASPOSE_ASSERT_EQ(shapes[0]->get_Width(), shapes[1]->get_Width());
ASPOSE_ASSERT_EQ(shapes[0]->get_Height(), shapes[1]->get_Height());
ASSERT_EQ(shapes[0]->get_ShapeType(), shapes[1]->get_ShapeType());

// 第一个形状没有任何效果，第二个形状有阴影和粗轮廓。
// 这些效果使第二个形状的轮廓尺寸大于第一个形状。
// 即使在 Microsoft Word 中单击这些形状时矩形的大小会显示出来，
// 第二个形状的可见外部边界受到阴影和轮廓的影响，因此更大。
// 我们可以使用 "AdjustWithEffects" 方法来查看形状的真实大小。
ASPOSE_ASSERT_EQ(0.0, shapes[0]->get_StrokeWeight());
ASPOSE_ASSERT_EQ(20.0, shapes[1]->get_StrokeWeight());
ASSERT_FALSE(shapes[0]->get_ShadowEnabled());
ASSERT_TRUE(shapes[1]->get_ShadowEnabled());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = shapes[0];

// 创建一个 RectangleF 对象，表示一个矩形，
// 我们可能可以将其用作形状的坐标和边界。
System::Drawing::RectangleF rectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);

// 运行此方法以获取考虑所有形状效果后矩形的大小。
System::Drawing::RectangleF rectangleFOut = shape->AdjustWithEffects(rectangleF);

// 由于形状没有改变边框的效果，其边界尺寸不受影响。
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_Y());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Height());

// 验证第一个形状的最终范围（以点为单位）。
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Height());

shape = shapes[1];
rectangleF = System::Drawing::RectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);
rectangleFOut = shape->AdjustWithEffects(rectangleF);

// 形状效果已将形状的表观左上角略微移动。
ASPOSE_ASSERT_EQ(171.5, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(167, rectangleFOut.get_Y());

// 这些效果还影响了形状的可见尺寸。
ASPOSE_ASSERT_EQ(1045, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1133.5, rectangleFOut.get_Height());

// 这些效果还影响了形状的可见边界。
ASPOSE_ASSERT_EQ(-28.5, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(-33, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(192, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(280.5, shape->get_BoundsWithEffects().get_Height());
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

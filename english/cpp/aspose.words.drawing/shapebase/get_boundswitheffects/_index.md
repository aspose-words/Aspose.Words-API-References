---
title: Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects method
linktitle: get_BoundsWithEffects
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects method. Gets final extent that this shape object has after applying drawing effects. Value is measured in points in C++.'
type: docs
weight: 61144
url: /cpp/aspose.words.drawing/shapebase/get_boundswitheffects/
---
## ShapeBase::get_BoundsWithEffects method


Gets final extent that this shape object has after applying drawing effects. Value is measured in points.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects()
```

## Examples


Shows how to check how a shape's bounds are affected by shape effects.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Shape shadow effect.docx"));

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape>>()->LINQ_ToArray();

ASSERT_EQ(shapes->get_Length(), 2);

// The two shapes are identical in terms of dimensions and shape type.
ASPOSE_ASSERT_EQ(shapes[1]->get_Width(), shapes[0]->get_Width());
ASPOSE_ASSERT_EQ(shapes[1]->get_Height(), shapes[0]->get_Height());
ASSERT_EQ(shapes[1]->get_ShapeType(), shapes[0]->get_ShapeType());

// The first shape has no effects, and the second one has a shadow and thick outline.
// These effects make the size of the second shape's silhouette bigger than that of the first.
// Even though the rectangle's size shows up when we click on these shapes in Microsoft Word,
// the visible outer bounds of the second shape are affected by the shadow and outline and thus are bigger.
// We can use the "AdjustWithEffects" method to see the true size of the shape.
ASPOSE_ASSERT_EQ(shapes[0]->get_StrokeWeight(), 0.0);
ASPOSE_ASSERT_EQ(shapes[1]->get_StrokeWeight(), 20.0);
ASSERT_FALSE(shapes[0]->get_ShadowEnabled());
ASSERT_TRUE(shapes[1]->get_ShadowEnabled());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = shapes[0];

// Create a RectangleF object, representing a rectangle,
// which we could potentially use as the coordinates and bounds for a shape.
System::Drawing::RectangleF rectangleF(static_cast<float>(200.0f), static_cast<float>(200.0f), static_cast<float>(1000.0f), static_cast<float>(1000.0f));

// Run this method to get the size of the rectangle adjusted for all our shape effects.
System::Drawing::RectangleF rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Since the shape has no border-changing effects, its boundary dimensions are unaffected.
ASPOSE_ASSERT_EQ(rectangleFOut.get_X(), 200);
ASPOSE_ASSERT_EQ(rectangleFOut.get_Y(), 200);
ASPOSE_ASSERT_EQ(rectangleFOut.get_Width(), 1000);
ASPOSE_ASSERT_EQ(rectangleFOut.get_Height(), 1000);

// Verify the final extent of the first shape, in points.
ASPOSE_ASSERT_EQ(shape->get_BoundsWithEffects().get_X(), 0);
ASPOSE_ASSERT_EQ(shape->get_BoundsWithEffects().get_Y(), 0);
ASPOSE_ASSERT_EQ(shape->get_BoundsWithEffects().get_Width(), 147);
ASPOSE_ASSERT_EQ(shape->get_BoundsWithEffects().get_Height(), 147);

shape = shapes[1];
rectangleF = System::Drawing::RectangleF(static_cast<float>(200.0f), static_cast<float>(200.0f), static_cast<float>(1000.0f), static_cast<float>(1000.0f));
rectangleFOut = shape->AdjustWithEffects(rectangleF);

// The shape effects have moved the apparent top left corner of the shape slightly.
ASPOSE_ASSERT_EQ(rectangleFOut.get_X(), 171.5);
ASPOSE_ASSERT_EQ(rectangleFOut.get_Y(), 167);

// The effects have also affected the visible dimensions of the shape.
ASPOSE_ASSERT_EQ(rectangleFOut.get_Width(), 1045);
ASPOSE_ASSERT_EQ(rectangleFOut.get_Height(), 1133.5);

// The effects have also affected the visible bounds of the shape.
ASPOSE_ASSERT_EQ(shape->get_BoundsWithEffects().get_X(), -28.5);
ASPOSE_ASSERT_EQ(shape->get_BoundsWithEffects().get_Y(), -33);
ASPOSE_ASSERT_EQ(shape->get_BoundsWithEffects().get_Width(), 192);
ASPOSE_ASSERT_EQ(shape->get_BoundsWithEffects().get_Height(), 280.5);
```
## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

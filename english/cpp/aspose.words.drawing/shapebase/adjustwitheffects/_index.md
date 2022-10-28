---
title: AdjustWithEffects
second_title: Aspose.Words for C++ API Reference
description: Adds to the source rectangle values of the effect extent and returns the final rectangle.
type: docs
weight: 1
url: /cpp/aspose.words.drawing/shapebase/adjustwitheffects/
---
## ShapeBase.AdjustWithEffects method


Adds to the source rectangle values of the effect extent and returns the final rectangle.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::AdjustWithEffects(System::Drawing::RectangleF source)
```


## Examples




Shows how to check how a shape's bounds are affected by shape effects. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Shape shadow effect.docx");

ArrayPtr<SharedPtr<Shape>> shapes = doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<SharedPtr<Shape>>()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// The two shapes are identical in terms of dimensions and shape type.
ASPOSE_ASSERT_EQ(shapes[0]->get_Width(), shapes[1]->get_Width());
ASPOSE_ASSERT_EQ(shapes[0]->get_Height(), shapes[1]->get_Height());
ASSERT_EQ(shapes[0]->get_ShapeType(), shapes[1]->get_ShapeType());

// The first shape has no effects, and the second one has a shadow and thick outline.
// These effects make the size of the second shape's silhouette bigger than that of the first.
// Even though the rectangle's size shows up when we click on these shapes in Microsoft Word,
// the visible outer bounds of the second shape are affected by the shadow and outline and thus are bigger.
// We can use the "AdjustWithEffects" method to see the true size of the shape.
ASPOSE_ASSERT_EQ(0.0, shapes[0]->get_StrokeWeight());
ASPOSE_ASSERT_EQ(20.0, shapes[1]->get_StrokeWeight());
ASSERT_FALSE(shapes[0]->get_ShadowEnabled());
ASSERT_TRUE(shapes[1]->get_ShadowEnabled());

SharedPtr<Shape> shape = shapes[0];

// Create a RectangleF object, representing a rectangle,
// which we could potentially use as the coordinates and bounds for a shape.
System::Drawing::RectangleF rectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);

// Run this method to get the size of the rectangle adjusted for all our shape effects.
System::Drawing::RectangleF rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Since the shape has no border-changing effects, its boundary dimensions are unaffected.
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_Y());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Height());

// Verify the final extent of the first shape, in points.
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Height());

shape = shapes[1];
rectangleF = System::Drawing::RectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);
rectangleFOut = shape->AdjustWithEffects(rectangleF);

// The shape effects have moved the apparent top left corner of the shape slightly.
ASPOSE_ASSERT_EQ(171.5, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(167, rectangleFOut.get_Y());

// The effects have also affected the visible dimensions of the shape.
ASPOSE_ASSERT_EQ(1045, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1132, rectangleFOut.get_Height());

// The effects have also affected the visible bounds of the shape.
ASPOSE_ASSERT_EQ(-28.5, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(-33, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(192, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(279, shape->get_BoundsWithEffects().get_Height());
```


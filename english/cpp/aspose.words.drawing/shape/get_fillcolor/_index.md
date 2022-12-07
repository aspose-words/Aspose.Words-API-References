---
title: get_FillColor
second_title: Aspose.Words for C++ API Reference
description: Defines the brush color that fills the closed path of the shape.
type: docs
weight: 66
url: /cpp/aspose.words.drawing/shape/get_fillcolor/
---
## Shape::get_FillColor method


Defines the brush color that fills the closed path of the shape.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Shape::get_FillColor()
```

## Remarks


This is a shortcut to the [Color](../../fill/get_color/) property.

The default value is **White**.

## Examples



Shows how to fill a shape with a solid color. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Write some text, and then cover it with a floating shape.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

SharedPtr<Shape> shape = builder->InsertShape(ShapeType::CloudCallout, RelativeHorizontalPosition::LeftMargin, 25, RelativeVerticalPosition::TopMargin,
                                              25, 250, 150, WrapType::None);

// Use the "StrokeColor" property to set the color of the outline of the shape.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Use the "FillColor" property to set the color of the inside area of the shape.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// The "Opacity" property determines how transparent the color is on a 0-1 scale,
// with 1 being fully opaque, and 0 being invisible.
// The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(ArtifactsDir + u"Shape.Fill.docx");
```

## See Also

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)

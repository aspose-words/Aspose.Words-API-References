---
title: get_Opacity
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque).
type: docs
weight: 144
url: /cpp/aspose.words.drawing/fill/get_opacity/
---
## Fill::get_Opacity method


Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque).

```cpp
double Aspose::Words::Drawing::Fill::get_Opacity()
```


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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)

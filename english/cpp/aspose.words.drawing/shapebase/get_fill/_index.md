---
title: Aspose::Words::Drawing::ShapeBase::get_Fill method
linktitle: get_Fill
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_Fill method. Gets fill formatting for the shape in C++.'
type: docs
weight: 19000
url: /cpp/aspose.words.drawing/shapebase/get_fill/
---
## ShapeBase::get_Fill method


Gets fill formatting for the shape.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Fill> Aspose::Words::Drawing::ShapeBase::get_Fill()
```


## Examples



Shows how to fill a shape with a solid color. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Write some text, and then cover it with a floating shape.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

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

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## See Also

* Class [Fill](../../fill/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

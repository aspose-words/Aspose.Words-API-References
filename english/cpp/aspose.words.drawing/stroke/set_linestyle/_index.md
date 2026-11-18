---
title: Aspose::Words::Drawing::Stroke::set_LineStyle method
linktitle: set_LineStyle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Stroke::set_LineStyle method. Defines the line style of the stroke in C++.'
type: docs
weight: 34000
url: /cpp/aspose.words.drawing/stroke/set_linestyle/
---
## Stroke::set_LineStyle method


Defines the line style of the stroke.

```cpp
void Aspose::Words::Drawing::Stroke::set_LineStyle(Aspose::Words::Drawing::ShapeLineStyle value)
```

## Remarks


The default value is [Single](../../shapelinestyle/).
## Examples


Shows how change stroke properties.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(ShapeType::Rectangle, RelativeHorizontalPosition::LeftMargin, static_cast<double>(100), RelativeVerticalPosition::TopMargin, static_cast<double>(100), static_cast<double>(200), static_cast<double>(200), WrapType::None);

// Basic shapes, such as the rectangle, have two visible parts.
// 1 -  The fill, which applies to the area within the outline of the shape:
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  The stroke, which marks the outline of the shape:
// Modify various properties of this shape's stroke.
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_On(true);
stroke->set_Weight(5);
stroke->set_Color(System::Drawing::Color::get_Red());
stroke->set_DashStyle(DashStyle::ShortDashDotDot);
stroke->set_JoinStyle(JoinStyle::Miter);
stroke->set_EndCap(EndCap::Square);
stroke->set_LineStyle(ShapeLineStyle::Triple);
stroke->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Red(), System::Drawing::Color::get_Blue(), GradientStyle::Vertical, GradientVariant::Variant1);

doc->Save(get_ArtifactsDir() + u"Shape.Stroke.docx");
```
## See Also

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

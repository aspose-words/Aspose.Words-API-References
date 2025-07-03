---
title: Aspose::Words::Drawing::Stroke::get_LineStyle method
linktitle: get_LineStyle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Stroke::get_LineStyle method. Defines the line style of the stroke in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.drawing/stroke/get_linestyle/
---
## Stroke::get_LineStyle method


Defines the line style of the stroke.

```cpp
Aspose::Words::Drawing::ShapeLineStyle Aspose::Words::Drawing::Stroke::get_LineStyle()
```

## Remarks


The default value is [Single](../../shapelinestyle/).

## Examples



Shows how change stroke properties. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// Basic shapes, such as the rectangle, have two visible parts.
// 1 -  The fill, which applies to the area within the outline of the shape:
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  The stroke, which marks the outline of the shape:
// Modify various properties of this shape's stroke.
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_On(true);
stroke->set_Weight(5);
stroke->set_Color(System::Drawing::Color::get_Red());
stroke->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDashDotDot);
stroke->set_JoinStyle(Aspose::Words::Drawing::JoinStyle::Miter);
stroke->set_EndCap(Aspose::Words::Drawing::EndCap::Square);
stroke->set_LineStyle(Aspose::Words::Drawing::ShapeLineStyle::Triple);
stroke->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Red(), System::Drawing::Color::get_Blue(), Aspose::Words::Drawing::GradientStyle::Vertical, Aspose::Words::Drawing::GradientVariant::Variant1);

doc->Save(get_ArtifactsDir() + u"Shape.Stroke.docx");
```

## See Also

* Enum [ShapeLineStyle](../../shapelinestyle/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

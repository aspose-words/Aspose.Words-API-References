---
title: get_LineStyle
second_title: Aspose.Words for C++ API Reference
description: Defines the line style of the stroke.
type: docs
weight: 157
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertShape(ShapeType::Rectangle, RelativeHorizontalPosition::LeftMargin, 100, RelativeVerticalPosition::TopMargin,
                                              100, 200, 200, WrapType::None);

// Basic shapes, such as the rectangle, have two visible parts.
// 1 -  The fill, which applies to the area within the outline of the shape:
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  The stroke, which marks the outline of the shape:
// Modify various properties of this shape's stroke.
SharedPtr<Stroke> stroke = shape->get_Stroke();
stroke->set_On(true);
stroke->set_Weight(5);
stroke->set_Color(System::Drawing::Color::get_Red());
stroke->set_DashStyle(DashStyle::ShortDashDotDot);
stroke->set_JoinStyle(JoinStyle::Miter);
stroke->set_EndCap(EndCap::Square);
stroke->set_LineStyle(ShapeLineStyle::Triple);

doc->Save(ArtifactsDir + u"Shape.Stroke.docx");
```

## See Also

* Enum [ShapeLineStyle](../../shapelinestyle/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)

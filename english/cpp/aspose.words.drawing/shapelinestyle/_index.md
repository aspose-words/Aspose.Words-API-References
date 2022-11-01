---
title: ShapeLineStyle
second_title: Aspose.Words for C++ API Reference
description: Specifies the compound line style of a Shape.
type: docs
weight: 456
url: /cpp/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enum


Specifies the compound line style of a [Shape](../shape/).

### Values

| Name | Value | Description |
| --- | --- | --- |
| Single | 0 | Single line. |
| Double | 1 | Double lines of equal width. |
| ThickThin | 2 | Double lines, one thick, one thin. |
| ThinThick | 3 | Double lines, one thin, one thick. |
| Triple | 4 | Three lines, thin, thick, thin. |
| Default | n/a | Default value is **Single**. |


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


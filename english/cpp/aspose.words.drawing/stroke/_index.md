---
title: Stroke
second_title: Aspose.Words for C++ API Reference
description: Defines a stroke for a shape. To learn more, visit the  documentation article.
type: docs
weight: 170
url: /cpp/aspose.words.drawing/stroke/
---
## Stroke class


Defines a stroke for a shape. To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) documentation article.

```cpp
class Stroke : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Gets or sets the background color of the stroke. |
| [get_Color](./get_color/)() | Defines the color of a stroke. |
| [get_Color2](./get_color2/)() | Defines a second color for a stroke. |
| [get_DashStyle](./get_dashstyle/)() | Specifies the dot and dash pattern for a stroke. |
| [get_EndArrowLength](./get_endarrowlength/)() | Defines the arrowhead length for the end of a stroke. |
| [get_EndArrowType](./get_endarrowtype/)() | Defines the arrowhead for the end of a stroke. |
| [get_EndArrowWidth](./get_endarrowwidth/)() | Defines the arrowhead width for the end of a stroke. |
| [get_EndCap](./get_endcap/)() | Defines the cap style for the end of a stroke. |
| [get_ForeColor](./get_forecolor/)() | Gets or sets the foreground color of the stroke. |
| [get_ImageBytes](./get_imagebytes/)() | Defines the image for a stroke image or pattern fill. |
| [get_JoinStyle](./get_joinstyle/)() | Defines the join style of a polyline. |
| [get_LineStyle](./get_linestyle/)() | Defines the line style of the stroke. |
| [get_On](./get_on/)() | Defines whether the path will be stroked. |
| [get_Opacity](./get_opacity/)() | Defines the amount of transparency of a stroke. Valid range is from 0 to 1. |
| [get_StartArrowLength](./get_startarrowlength/)() | Defines the arrowhead length for the start of a stroke. |
| [get_StartArrowType](./get_startarrowtype/)() | Defines the arrowhead for the start of a stroke. |
| [get_StartArrowWidth](./get_startarrowwidth/)() | Defines the arrowhead width for the start of a stroke. |
| [get_Transparency](./get_transparency/)() | Gets or sets a value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency of the stroke. |
| [get_Visible](./get_visible/)() | Gets or sets a flag indicating whether the stroke is visible. |
| [get_Weight](./get_weight/)() | Defines the brush thickness that strokes the path of a shape in points. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Drawing::Stroke::get_BackColor](./get_backcolor/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter for [Aspose::Words::Drawing::Stroke::get_Color](./get_color/). |
| [set_Color2](./set_color2/)(System::Drawing::Color) | Setter for [Aspose::Words::Drawing::Stroke::get_Color2](./get_color2/). |
| [set_DashStyle](./set_dashstyle/)(Aspose::Words::Drawing::DashStyle) | Setter for [Aspose::Words::Drawing::Stroke::get_DashStyle](./get_dashstyle/). |
| [set_EndArrowLength](./set_endarrowlength/)(Aspose::Words::Drawing::ArrowLength) | Setter for [Aspose::Words::Drawing::Stroke::get_EndArrowLength](./get_endarrowlength/). |
| [set_EndArrowType](./set_endarrowtype/)(Aspose::Words::Drawing::ArrowType) | Setter for [Aspose::Words::Drawing::Stroke::get_EndArrowType](./get_endarrowtype/). |
| [set_EndArrowWidth](./set_endarrowwidth/)(Aspose::Words::Drawing::ArrowWidth) | Setter for [Aspose::Words::Drawing::Stroke::get_EndArrowWidth](./get_endarrowwidth/). |
| [set_EndCap](./set_endcap/)(Aspose::Words::Drawing::EndCap) | Setter for [Aspose::Words::Drawing::Stroke::get_EndCap](./get_endcap/). |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Drawing::Stroke::get_ForeColor](./get_forecolor/). |
| [set_JoinStyle](./set_joinstyle/)(Aspose::Words::Drawing::JoinStyle) | Setter for [Aspose::Words::Drawing::Stroke::get_JoinStyle](./get_joinstyle/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::Drawing::ShapeLineStyle) | Setter for [Aspose::Words::Drawing::Stroke::get_LineStyle](./get_linestyle/). |
| [set_On](./set_on/)(bool) | Setter for [Aspose::Words::Drawing::Stroke::get_On](./get_on/). |
| [set_Opacity](./set_opacity/)(double) | Setter for [Aspose::Words::Drawing::Stroke::get_Opacity](./get_opacity/). |
| [set_StartArrowLength](./set_startarrowlength/)(Aspose::Words::Drawing::ArrowLength) | Setter for [Aspose::Words::Drawing::Stroke::get_StartArrowLength](./get_startarrowlength/). |
| [set_StartArrowType](./set_startarrowtype/)(Aspose::Words::Drawing::ArrowType) | Setter for [Aspose::Words::Drawing::Stroke::get_StartArrowType](./get_startarrowtype/). |
| [set_StartArrowWidth](./set_startarrowwidth/)(Aspose::Words::Drawing::ArrowWidth) | Setter for [Aspose::Words::Drawing::Stroke::get_StartArrowWidth](./get_startarrowwidth/). |
| [set_Transparency](./set_transparency/)(double) | Setter for [Aspose::Words::Drawing::Stroke::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | Setter for [Aspose::Words::Drawing::Stroke::get_Visible](./get_visible/). |
| [set_Weight](./set_weight/)(double) | Setter for [Aspose::Words::Drawing::Stroke::get_Weight](./get_weight/). |
| static [Type](./type/)() |  |
## Remarks


Use the [Stroke](../shape/get_stroke/) property to access stroke properties of a shape. You do not create instances of the [Stroke](./) class directly.

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words](../../)

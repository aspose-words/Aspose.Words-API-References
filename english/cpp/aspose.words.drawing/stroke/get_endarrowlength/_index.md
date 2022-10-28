---
title: get_EndArrowLength
second_title: Aspose.Words for C++ API Reference
description: Defines the arrowhead length for the end of a stroke.
type: docs
weight: 53
url: /cpp/aspose.words.drawing/stroke/get_endarrowlength/
---
## Stroke.get_EndArrowLength method


Defines the arrowhead length for the end of a stroke.

```cpp
Aspose::Words::Drawing::ArrowLength Aspose::Words::Drawing::Stroke::get_EndArrowLength()
```


The default value is **Medium**.

## Examples




Shows to create a variety of shapes. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are four examples of shapes that we can insert into our documents.
// 1 -  Dotted, horizontal, half-transparent red line
// with an arrow on the left end and a diamond on the right end:
auto arrow = MakeObject<Shape>(doc, ShapeType::Line);
arrow->set_Width(200);
arrow->get_Stroke()->set_Color(System::Drawing::Color::get_Red());
arrow->get_Stroke()->set_StartArrowType(ArrowType::Arrow);
arrow->get_Stroke()->set_StartArrowLength(ArrowLength::Long);
arrow->get_Stroke()->set_StartArrowWidth(ArrowWidth::Wide);
arrow->get_Stroke()->set_EndArrowType(ArrowType::Diamond);
arrow->get_Stroke()->set_EndArrowLength(ArrowLength::Long);
arrow->get_Stroke()->set_EndArrowWidth(ArrowWidth::Wide);
arrow->get_Stroke()->set_DashStyle(DashStyle::Dash);
arrow->get_Stroke()->set_Opacity(0.5);

ASSERT_EQ(JoinStyle::Miter, arrow->get_Stroke()->get_JoinStyle());

builder->InsertNode(arrow);

// 2 -  Thick black diagonal line with rounded ends:
auto line = MakeObject<Shape>(doc, ShapeType::Line);
line->set_Top(40);
line->set_Width(200);
line->set_Height(20);
line->set_StrokeWeight(5.0);
line->get_Stroke()->set_EndCap(EndCap::Round);

builder->InsertNode(line);

// 3 -  Arrow with a green fill:
auto filledInArrow = MakeObject<Shape>(doc, ShapeType::Arrow);
filledInArrow->set_Width(200);
filledInArrow->set_Height(40);
filledInArrow->set_Top(100);
filledInArrow->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());
filledInArrow->get_Fill()->set_Visible(true);

builder->InsertNode(filledInArrow);

// 4 -  Arrow with a flipped orientation filled in with the Aspose logo:
auto filledInArrowImg = MakeObject<Shape>(doc, ShapeType::Arrow);
filledInArrowImg->set_Width(200);
filledInArrowImg->set_Height(40);
filledInArrowImg->set_Top(160);
filledInArrowImg->set_FlipOrientation(FlipOrientation::Both);

ArrayPtr<uint8_t> imageBytes = System::IO::File::ReadAllBytes(ImageDir + u"Logo.jpg");

{
    auto stream = MakeObject<System::IO::MemoryStream>(imageBytes);
    SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
    // When we flip the orientation of our arrow, we also flip the image that the arrow contains.
    // Flip the image the other way to cancel this out before getting the shape to display it.
    image->RotateFlip(System::Drawing::RotateFlipType::RotateNoneFlipXY);

    filledInArrowImg->get_ImageData()->SetImage(image);
    filledInArrowImg->get_Stroke()->set_JoinStyle(JoinStyle::Round);

    builder->InsertNode(filledInArrowImg);
}

doc->Save(ArtifactsDir + u"Drawing.VariousShapes.docx");
```


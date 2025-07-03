---
title: Aspose::Words::Drawing::Shape::Shape constructor
linktitle: Shape
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Shape::Shape constructor. Creates a new shape object in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.drawing/shape/shape/
---
## Shape::Shape constructor


Creates a new shape object.

```cpp
Aspose::Words::Drawing::Shape::Shape(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Drawing::ShapeType shapeType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
| shapeType | Aspose::Words::Drawing::ShapeType | The type of the shape to create. |
## Remarks


You should specify desired shape properties after you created a shape.

## Examples



Shows how to insert a shape with an image from the local file system into a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// The "Shape" class's public constructor will create a shape with "ShapeMarkupLanguage.Vml" markup type.
// If you need to create a shape of a non-primitive type, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
// please use DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


Shows how to create and format a text box. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Create a floating text box.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Set the horizontal, and vertical alignment of the text inside the shape.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Add a paragraph to the text box and add a run of text that the text box will display.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## See Also

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [ShapeType](../../shapetype/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

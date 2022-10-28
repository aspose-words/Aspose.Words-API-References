---
title: Shape
second_title: Aspose.Words for C++ API Reference
description: Creates a new shape object.
type: docs
weight: 1
url: /cpp/aspose.words.drawing/shape/shape/
---
## Shape.Shape method


Creates a new shape object.

```cpp
Aspose::Words::Drawing::Shape::Shape(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Drawing::ShapeType shapeType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
| shapeType | Aspose::Words::Drawing::ShapeType | The type of the shape to create. |

You should specify desired shape properties after you created a shape.

## Examples




Shows how to insert a shape with an image from the local file system into a document. 
```cpp
auto doc = MakeObject<Document>();

// The "Shape" class's public constructor will create a shape with "ShapeMarkupLanguage.Vml" markup type.
// If you need to create a shape of a non-primitive type, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
// please use DocumentBuilder.InsertShape.
auto shape = MakeObject<Shape>(doc, ShapeType::Image);
shape->get_ImageData()->SetImage(ImageDir + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(shape);

doc->Save(ArtifactsDir + u"Image.FromFile.docx");
```


Shows how to create and format a text box. 
```cpp
auto doc = MakeObject<Document>();

// Create a floating text box.
auto textBox = MakeObject<Shape>(doc, ShapeType::TextBox);
textBox->set_WrapType(WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Set the horizontal, and vertical alignment of the text inside the shape.
textBox->set_HorizontalAlignment(HorizontalAlignment::Center);
textBox->set_VerticalAlignment(VerticalAlignment::Top);

// Add a paragraph to the text box and add a run of text that the text box will display.
textBox->AppendChild(MakeObject<Paragraph>(doc));
SharedPtr<Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);
auto run = MakeObject<Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(textBox);

doc->Save(ArtifactsDir + u"Shape.CreateTextBox.docx");
```


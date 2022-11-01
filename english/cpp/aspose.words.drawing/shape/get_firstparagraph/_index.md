---
title: get_FirstParagraph
second_title: Aspose.Words for C++ API Reference
description: Gets the first paragraph in the shape.
type: docs
weight: 79
url: /cpp/aspose.words.drawing/shape/get_firstparagraph/
---
## Shape.get_FirstParagraph method


Gets the first paragraph in the shape.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::Shape::get_FirstParagraph()
```


## Examples




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


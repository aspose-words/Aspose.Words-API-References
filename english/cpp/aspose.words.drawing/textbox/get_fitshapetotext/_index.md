---
title: Aspose::Words::Drawing::TextBox::get_FitShapeToText method
linktitle: get_FitShapeToText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextBox::get_FitShapeToText method. Determines whether Microsoft Word will grow the shape to fit text in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.drawing/textbox/get_fitshapetotext/
---
## TextBox::get_FitShapeToText method


Determines whether Microsoft Word will grow the shape to fit text.

```cpp
bool Aspose::Words::Drawing::TextBox::get_FitShapeToText()
```

## Remarks


The default value is **false**.

## Examples



Shows how to get a text box to resize itself to fit its contents tightly. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Apply these values to both these members to get the parent shape to fit
// tightly around the text contents, ignoring the dimensions we have set.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```

## See Also

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

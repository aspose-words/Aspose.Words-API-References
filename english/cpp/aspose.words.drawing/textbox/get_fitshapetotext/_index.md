---
title: get_FitShapeToText
second_title: Aspose.Words for C++ API Reference
description: Determines whether Microsoft Word will grow the shape to fit text.
type: docs
weight: 14
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> textBoxShape = builder->InsertShape(ShapeType::TextBox, 150, 100);
SharedPtr<TextBox> textBox = textBoxShape->get_TextBox();

// Apply these values to both these members to get the parent shape to fit
// tightly around the text contents, ignoring the dimensions we have set.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(ArtifactsDir + u"Shape.TextBoxFitShapeToText.docx");
```

## See Also

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)

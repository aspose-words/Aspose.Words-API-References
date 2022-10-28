---
title: get_InternalMarginTop
second_title: Aspose.Words for C++ API Reference
description: Specifies the inner top margin in points for a shape.
type: docs
weight: 66
url: /cpp/aspose.words.drawing/textbox/get_internalmargintop/
---
## TextBox.get_InternalMarginTop method


Specifies the inner top margin in points for a shape.

```cpp
double Aspose::Words::Drawing::TextBox::get_InternalMarginTop()
```


The default value is 1/20 inch.

## Examples




Shows how to set internal margins for a text box. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert another textbox with specific margins.
SharedPtr<Shape> textBoxShape = builder->InsertShape(ShapeType::TextBox, 100, 100);
SharedPtr<TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(ArtifactsDir + u"Shape.TextBoxMargins.docx");
```


---
title: Aspose::Words::Drawing::TextBox::get_InternalMarginRight method
linktitle: get_InternalMarginRight
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextBox::get_InternalMarginRight method. Specifies the inner right margin in points for a shape in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.drawing/textbox/get_internalmarginright/
---
## TextBox::get_InternalMarginRight method


Specifies the inner right margin in points for a shape.

```cpp
double Aspose::Words::Drawing::TextBox::get_InternalMarginRight()
```

## Remarks


The default value is 1/10 inch.

## Examples



Shows how to set internal margins for a text box. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert another textbox with specific margins.
System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxMargins.docx");
```

## See Also

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

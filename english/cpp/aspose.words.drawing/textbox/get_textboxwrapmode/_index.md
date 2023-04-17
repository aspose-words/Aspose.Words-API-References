---
title: Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode method
linktitle: get_TextBoxWrapMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode method. Determines how text wraps inside a shape in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.drawing/textbox/get_textboxwrapmode/
---
## TextBox::get_TextBoxWrapMode method


Determines how text wraps inside a shape.

```cpp
Aspose::Words::Drawing::TextBoxWrapMode Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode()
```

## Remarks


The default value is [Square](../../textboxwrapmode/).

## Examples



Shows how to set a wrapping mode for the contents of a text box. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> textBoxShape = builder->InsertShape(ShapeType::TextBox, 300, 300);
SharedPtr<TextBox> textBox = textBoxShape->get_TextBox();

// Set the "TextBoxWrapMode" property to "TextBoxWrapMode.None" to increase the text box's width
// to accommodate text, should it be large enough.
// Set the "TextBoxWrapMode" property to "TextBoxWrapMode.Square" to
// wrap all text inside the text box, preserving its dimensions.
textBox->set_TextBoxWrapMode(textBoxWrapMode);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->get_Font()->set_Size(32);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(ArtifactsDir + u"Shape.TextBoxContentsWrapMode.docx");
```

## See Also

* Enum [TextBoxWrapMode](../../textboxwrapmode/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

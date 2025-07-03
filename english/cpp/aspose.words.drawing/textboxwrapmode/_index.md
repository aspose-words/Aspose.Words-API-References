---
title: Aspose::Words::Drawing::TextBoxWrapMode enum
linktitle: TextBoxWrapMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextBoxWrapMode enum. Specifies how text wraps inside a shape in C++.'
type: docs
weight: 40000
url: /cpp/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enum


Specifies how text wraps inside a shape.

```cpp
enum class TextBoxWrapMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Square | 0 | Text wraps inside a shape. |
| None | 2 | Text does not wrap inside a shape. |


## Examples



Shows how to set a wrapping mode for the contents of a text box. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 300);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Set the "TextBoxWrapMode" property to "TextBoxWrapMode.None" to increase the text box's width
// to accommodate text, should it be large enough.
// Set the "TextBoxWrapMode" property to "TextBoxWrapMode.Square" to
// wrap all text inside the text box, preserving its dimensions.
textBox->set_TextBoxWrapMode(textBoxWrapMode);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->get_Font()->set_Size(32);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxContentsWrapMode.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

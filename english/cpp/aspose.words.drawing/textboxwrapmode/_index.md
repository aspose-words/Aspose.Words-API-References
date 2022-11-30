---
title: TextBoxWrapMode
second_title: Aspose.Words for C++ API Reference
description: Specifies how text wraps inside a shape.
type: docs
weight: 508
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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words](../../)

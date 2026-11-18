---
title: Aspose::Words::Drawing::TextBox::set_VerticalAnchor method
linktitle: set_VerticalAnchor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextBox::set_VerticalAnchor method. Specifies the vertical alignment of the text within a shape in C++.'
type: docs
weight: 27000
url: /cpp/aspose.words.drawing/textbox/set_verticalanchor/
---
## TextBox::set_VerticalAnchor method


Specifies the vertical alignment of the text within a shape.

```cpp
void Aspose::Words::Drawing::TextBox::set_VerticalAnchor(Aspose::Words::Drawing::TextBoxAnchor value)
```

## Remarks


The default value is [Top](../../textboxanchor/).
## Examples


Shows how to vertically align the text contents of a text box.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(ShapeType::TextBox, static_cast<double>(200), static_cast<double>(200));

// Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
// align the text in this text box with the top side of the shape.
// Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
// align the text in this text box to the center of the shape.
// Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
// align the text in this text box to the bottom of the shape.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
doc->get_CompatibilityOptions()->OptimizeFor(MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```
## See Also

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

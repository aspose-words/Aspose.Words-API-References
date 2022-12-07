---
title: get_VerticalAnchor
second_title: Aspose.Words for C++ API Reference
description: Specifies the vertical alignment of the text within a shape.
type: docs
weight: 157
url: /cpp/aspose.words.drawing/textbox/get_verticalanchor/
---
## TextBox::get_VerticalAnchor method


Specifies the vertical alignment of the text within a shape.

```cpp
Aspose::Words::Drawing::TextBoxAnchor Aspose::Words::Drawing::TextBox::get_VerticalAnchor()
```

## Remarks


The default value is [Top](../../textboxanchor/).

## Examples



Shows how to vertically align the text contents of a text box. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertShape(ShapeType::TextBox, 200, 200);

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
doc->Save(ArtifactsDir + u"Shape.VerticalAnchor.docx");
```

## See Also

* Enum [TextBoxAnchor](../../textboxanchor/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)

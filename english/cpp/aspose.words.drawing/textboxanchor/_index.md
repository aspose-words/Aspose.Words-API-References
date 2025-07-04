---
title: Aspose::Words::Drawing::TextBoxAnchor enum
linktitle: TextBoxAnchor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::TextBoxAnchor enum. Specifies values used for shape text vertical alignment in C++.'
type: docs
weight: 39000
url: /cpp/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enum


Specifies values used for shape text vertical alignment.

```cpp
enum class TextBoxAnchor
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Top | 0 | Text is aligned to the top of the textbox. |
| Middle | 1 | Text is aligned to the middle of the textbox. |
| Bottom | 2 | Text is aligned to the bottom of the textbox. |
| TopCentered | 3 | Text is aligned to the top centered of the textbox. |
| MiddleCentered | 4 | Text is aligned to the middle centered of the textbox. |
| BottomCentered | 5 | Text is aligned to the bottom centered of the textbox. |
| TopBaseline | 6 | Text is aligned to the top baseline of the textbox. |
| BottomBaseline | 7 | Text is aligned to the bottom baseline of the textbox. |
| TopCenteredBaseline | 8 | Text is aligned to the top centered baseline of the textbox. |
| BottomCenteredBaseline | 9 | Text is aligned to the bottom centered baseline of the textbox. |


## Examples



Shows how to vertically align the text contents of a text box. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

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
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

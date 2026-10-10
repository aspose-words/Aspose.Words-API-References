---
title: "Aspose::Words::Drawing::TextBox::get_InternalMarginLeft metod"
linktitle: "get_InternalMarginLeft"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::TextBox::get_InternalMarginLeft metod. Anger den inre vänstra marginalen i punkter för en form i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.drawing/textbox/get_internalmarginleft/
---
## TextBox::get_InternalMarginLeft method


Anger den inre vänstra marginalen i punkter för en form.

```cpp
double Aspose::Words::Drawing::TextBox::get_InternalMarginLeft()
```

## Anmärkningar


Standardvärdet är 1/10 tum.

## Exempel



Visar hur man ställer in interna marginaler för en textruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en annan textruta med specifika marginaler.
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

## Se även

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

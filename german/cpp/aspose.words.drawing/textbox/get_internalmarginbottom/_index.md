---
title: "Aspose::Words::Drawing::TextBox::get_InternalMarginBottom Methode"
linktitle: "get_InternalMarginBottom"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::TextBox::get_InternalMarginBottom Methode. Gibt den inneren unteren Rand in Punkten für ein Shape in C++ an."
type: docs
weight: 4000
url: /de/cpp/aspose.words.drawing/textbox/get_internalmarginbottom/
---
## TextBox::get_InternalMarginBottom method


Gibt den inneren unteren Rand in Punkten für eine Form an.

```cpp
double Aspose::Words::Drawing::TextBox::get_InternalMarginBottom()
```

## Hinweise


Der Standardwert ist 1/20 Zoll.

## Beispiele



Zeigt, wie interne Ränder für eine Textbox festgelegt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine weitere Textbox mit bestimmten Rändern ein.
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

## Siehe auch

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

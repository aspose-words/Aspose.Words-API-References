---
title: "Aspose::Words::Drawing::TextBox::get_FitShapeToText Methode"
linktitle: "get_FitShapeToText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::TextBox::get_FitShapeToText Methode. Bestimmt, ob Microsoft Word die Form vergrößert, um den Text in C++ anzupassen."
type: docs
weight: 3000
url: /de/cpp/aspose.words.drawing/textbox/get_fitshapetotext/
---
## TextBox::get_FitShapeToText method


Bestimmt, ob Microsoft Word die Form vergrößert, um den Text anzupassen.

```cpp
bool Aspose::Words::Drawing::TextBox::get_FitShapeToText()
```

## Hinweise


Der Standardwert ist **false**.

## Beispiele



Zeigt, wie eine Textbox sich selbst so anpasst, dass sie ihren Inhalt eng umschließt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Wenden Sie diese Werte auf beide Mitglieder an, damit die übergeordnete Form passt
// eng um den Textinhalt herum, wobei die von uns festgelegten Abmessungen ignoriert werden.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```

## Siehe auch

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

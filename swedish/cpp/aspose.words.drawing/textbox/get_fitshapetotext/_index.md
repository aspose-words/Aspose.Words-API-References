---
title: "Aspose::Words::Drawing::TextBox::get_FitShapeToText‑metod"
linktitle: "get_FitShapeToText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::TextBox::get_FitShapeToText‑metod. Bestämmer om Microsoft Word kommer att förstora formen för att passa text i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.drawing/textbox/get_fitshapetotext/
---
## TextBox::get_FitShapeToText method


Bestämmer om Microsoft Word kommer att förstora formen för att passa texten.

```cpp
bool Aspose::Words::Drawing::TextBox::get_FitShapeToText()
```

## Anmärkningar


Standardvärdet är **false**.

## Exempel



Visar hur man får en textruta att ändra storlek så att den passar innehållet tätt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Applicera dessa värden på båda dessa medlemmar för att få föräldraformen att passa
// tätt runt textinnehållet, utan att ta hänsyn till de dimensioner vi har angett.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```

## Se även

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

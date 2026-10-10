---
title: "Aspose::Words::Drawing::TextBox::get_InternalMarginRight metodo"
linktitle: "get_InternalMarginRight"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::TextBox::get_InternalMarginRight metodo. Specifica il margine interno destro in punti per una forma in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.drawing/textbox/get_internalmarginright/
---
## TextBox::get_InternalMarginRight method


Specifica il margine interno destro in punti per una forma.

```cpp
double Aspose::Words::Drawing::TextBox::get_InternalMarginRight()
```

## Note


Il valore predefinito è 1/10 di pollice.

## Esempi



Mostra come impostare i margini interni per una casella di testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un'altra casella di testo con margini specifici.
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

## Vedi anche

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

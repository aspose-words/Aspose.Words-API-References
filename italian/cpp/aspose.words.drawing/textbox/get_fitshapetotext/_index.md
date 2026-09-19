---
title: "Aspose::Words::Drawing::TextBox::get_FitShapeToText metodo"
linktitle: "get_FitShapeToText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::TextBox::get_FitShapeToText metodo. Determina se Microsoft Word ingrandirà la forma per adattarla al testo in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing/textbox/get_fitshapetotext/
---
## TextBox::get_FitShapeToText method


Determina se Microsoft Word allargherà la forma per adattare il testo.

```cpp
bool Aspose::Words::Drawing::TextBox::get_FitShapeToText()
```

## Note


Il valore predefinito è **false**.

## Esempi



Mostra come far ridimensionare una casella di testo affinché si adatti strettamente al suo contenuto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Applica questi valori a entrambi i membri per far sì che la forma padre si adatti
// strettamente attorno al contenuto del testo, ignorando le dimensioni impostate.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```

## Vedi anche

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

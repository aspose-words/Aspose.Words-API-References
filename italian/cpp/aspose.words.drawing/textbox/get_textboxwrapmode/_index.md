---
title: "Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode metodo"
linktitle: "get_TextBoxWrapMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode metodo. Determina come il testo si avvolge all'interno di una forma in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.drawing/textbox/get_textboxwrapmode/
---
## TextBox::get_TextBoxWrapMode method


Determina come il testo avvolge all'interno di una forma.

```cpp
Aspose::Words::Drawing::TextBoxWrapMode Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode()
```

## Note


Il valore predefinito è [Square](../../textboxwrapmode/).

## Esempi



Mostra come impostare una modalità di avvolgimento per il contenuto di una casella di testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 300);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Imposta la proprietà "TextBoxWrapMode" su "TextBoxWrapMode.None" per aumentare la larghezza della casella di testo
// per contenere il testo, dovrebbe essere sufficientemente grande.
// Imposta la proprietà "TextBoxWrapMode" su "TextBoxWrapMode.Square" per
// avvolgere tutto il testo all'interno della casella di testo, preservandone le dimensioni.
textBox->set_TextBoxWrapMode(textBoxWrapMode);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->get_Font()->set_Size(32);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxContentsWrapMode.docx");
```

## Vedi anche

* Enum [TextBoxWrapMode](../../textboxwrapmode/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

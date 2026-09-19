---
title: "Aspose::Words::Drawing::TextBoxWrapMode enum"
linktitle: "TextBoxWrapMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::TextBoxWrapMode enum. Specifica come il testo viene avvolto all'interno di una forma in C++."
type: docs
weight: 40000
url: /it/cpp/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enum


Specifica come il testo avvolge all'interno di una forma.

```cpp
enum class TextBoxWrapMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Square | 0 | Il testo si avvolge all'interno di una forma. |
| None | 2 | Il testo non si avvolge all'interno di una forma. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

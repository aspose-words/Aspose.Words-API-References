---
title: "Aspose::Words::Drawing::TextBox::get_LayoutFlow metodo"
linktitle: "get_LayoutFlow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::TextBox::get_LayoutFlow metodo. Determina il flusso del layout del testo in una forma in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.drawing/textbox/get_layoutflow/
---
## TextBox::get_LayoutFlow method


Determina il flusso del layout del testo in una forma.

```cpp
Aspose::Words::Drawing::LayoutFlow Aspose::Words::Drawing::TextBox::get_LayoutFlow()
```

## Note


Il valore predefinito è [Horizontal](../../layoutflow/).

## Esempi



Mostra come impostare l'orientamento del testo all'interno di una casella di testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Sposta il costruttore del documento all'interno della TextBox e aggiungi del testo.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Imposta la proprietà "LayoutFlow" per definire un orientamento per il contenuto testuale di questa casella di testo.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```

## Vedi anche

* Enum [LayoutFlow](../../layoutflow/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

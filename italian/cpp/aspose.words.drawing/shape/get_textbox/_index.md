---
title: "Aspose::Words::Drawing::Shape::get_TextBox metodo"
linktitle: "get_TextBox"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Shape::get_TextBox metodo. Definisce gli attributi che specificano come il testo è visualizzato in una shape in C++."
type: docs
weight: 24000
url: /it/cpp/aspose.words.drawing/shape/get_textbox/
---
## Shape::get_TextBox method


Definisce gli attributi che specificano come il testo è visualizzato in una forma.

```cpp
System::SharedPtr<Aspose::Words::Drawing::TextBox> Aspose::Words::Drawing::Shape::get_TextBox()
```


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

* Class [TextBox](../../textbox/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

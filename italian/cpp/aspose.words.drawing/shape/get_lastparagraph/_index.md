---
title: "Aspose::Words::Drawing::Shape::get_LastParagraph metodo"
linktitle: "get_LastParagraph"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Shape::get_LastParagraph metodo. Ottiene l'ultimo paragrafo nella shape in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.drawing/shape/get_lastparagraph/
---
## Shape::get_LastParagraph method


Ottiene l'ultimo paragrafo nella forma.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::Shape::get_LastParagraph()
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

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

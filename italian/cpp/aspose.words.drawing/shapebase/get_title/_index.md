---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_Title"
linktitle: "get_Title"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_Title. Ottiene o imposta il titolo (didascalia) dell'oggetto forma corrente in C++."
type: docs
weight: 51000
url: /it/cpp/aspose.words.drawing/shapebase/get_title/
---
## ShapeBase::get_Title method


Ottiene o imposta il titolo (didascalia) dell'oggetto forma corrente.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Title()
```

## Note


Il valore predefinito è una stringa vuota.

Non può essere **null**, ma può essere una stringa vuota.

## Esempi



Mostra come impostare il titolo di una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea una forma, assegnale un titolo, e poi aggiungila al documento.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_Width(200);
shape->set_Height(200);
shape->set_Title(u"My cube");

builder->InsertNode(shape);

// Quando salviamo un documento con una forma che ha un titolo,
// Aspose.Words memorizzerà quel titolo nel testo alternativo della forma.
doc->Save(get_ArtifactsDir() + u"Shape.Title.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Title.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::String::Empty, shape->get_Title());
ASSERT_EQ(u"Title: My cube", shape->get_AlternativeText());
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

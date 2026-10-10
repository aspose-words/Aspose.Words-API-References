---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision metodo"
linktitle: "get_IsInsertRevision"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision metodo. Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il tracciamento delle modifiche era abilitato in C++."
type: docs
weight: 31000
url: /it/cpp/aspose.words.drawing/shapebase/get_isinsertrevision/
---
## ShapeBase::get_IsInsertRevision method


Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il tracciamento delle modifiche era abilitato.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision()
```


## Esempi



Mostra come lavorare con le forme di revisione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_TrackRevisions());

// Inserisci una forma in linea senza tracciare le revisioni, il che farà sì che questa forma non sia una revisione di alcun tipo.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Inizia a tracciare le revisioni e poi inserisci un'altra forma, che sarà una revisione.
doc->StartTrackRevisions(u"John Doe");

shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Sun);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

shapes[0]->Remove();

// Poiché abbiamo rimosso quella forma mentre stavamo tracciando le modifiche,
// la forma persiste nel documento e conta come una revisione di eliminazione.
// Accettare questa revisione rimuoverà la forma in modo permanente, e rifiutarla la manterrà nel documento.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Cube, shapes[0]->get_ShapeType());
ASSERT_TRUE(shapes[0]->get_IsDeleteRevision());

// E abbiamo inserito un'altra forma mentre tracciavamo le modifiche, quindi quella forma conterà come una revisione di inserimento.
// Accettare questa revisione assimilerà questa forma nel documento come una non-revisione,
// e rifiutare la revisione rimuoverà questa forma in modo permanente.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Sun, shapes[1]->get_ShapeType());
ASSERT_TRUE(shapes[1]->get_IsInsertRevision());
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

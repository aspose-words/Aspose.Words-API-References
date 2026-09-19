---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInline metodo"
linktitle: "get_IsInline"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInline metodo. Un modo rapido per determinare se questa forma è posizionata in linea con il testo in C++."
type: docs
weight: 30000
url: /it/cpp/aspose.words.drawing/shapebase/get_isinline/
---
## ShapeBase::get_IsInline method


Un modo rapido per determinare se questa forma è posizionata in linea con il testo.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInline()
```

## Note


Ha effetto solo per le forme di livello superiore.

## Esempi



Mostra come determinare se una forma è in linea o fluttuante.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due tipi di avvolgimento che le forme possono avere.
// 1 -  In linea:
builder->Write(u"Hello world! ");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());
builder->Write(u" Hello again.");

// Una forma in linea si trova all'interno di un paragrafo insieme ad altri elementi del paragrafo, come sequenze di testo.
// In Microsoft Word, possiamo fare clic e trascinare la forma in qualsiasi paragrafo come se fosse un carattere.
// Se la forma è grande, influenzerà la spaziatura verticale del paragrafo.
// Non possiamo spostare questa forma in un punto senza paragrafo.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::Inline, shape->get_WrapType());
ASSERT_TRUE(shape->get_IsInline());

// 2 -  Fluttuante:
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

// Una forma fluttuante appartiene al paragrafo in cui la inseriamo,
// che possiamo determinare tramite un simbolo di ancoraggio che appare quando clicchiamo sulla forma.
// Se la forma non ha un simbolo di ancoraggio visibile a sinistra,
// dovremo abilitare gli ancoraggi visibili tramite "Opzioni" -> "Visualizza" -> "Ancoraggi oggetto".
// In Microsoft Word, possiamo fare clic sinistro e trascinare liberamente questa forma in qualsiasi posizione.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, shape->get_WrapType());
ASSERT_FALSE(shape->get_IsInline());

doc->Save(get_ArtifactsDir() + u"Shape.IsInline.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

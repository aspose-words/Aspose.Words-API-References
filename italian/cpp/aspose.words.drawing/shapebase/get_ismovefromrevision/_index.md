---
title: "Aspose::Words::Drawing::ShapeBase::get_IsMoveFromRevision metodo"
linktitle: "get_IsMoveFromRevision"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsMoveFromRevision metodo. Restituisce true se questo oggetto è stato spostato (cancellato) in Microsoft Word mentre il tracciamento delle modifiche era abilitato in C++."
type: docs
weight: 33000
url: /it/cpp/aspose.words.drawing/shapebase/get_ismovefromrevision/
---
## ShapeBase::get_IsMoveFromRevision method


Restituisce **true** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il tracciamento delle modifiche era abilitato.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsMoveFromRevision()
```


## Esempi



Mostra come identificare le forme di revisione di spostamento.
```cpp
// Una revisione di spostamento è quando spostiamo un elemento nel corpo del documento tagliandolo e incollandolo in Microsoft Word mentre
// tracciando le modifiche. Se includiamo una forma in linea in tale spostamento di testo, quella forma sarà anch'essa una revisione.
// Copiare e incollare o spostare forme fluttuanti non crea revisioni di spostamento.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision shape.docx");

// Le revisioni di spostamento consistono in coppie di revisioni "Move from" e "Move to". Abbiamo spostato in questo documento una forma,
// ma finché non accettiamo o rifiutiamo la revisione di spostamento, ci saranno due istanze di quella forma.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Questa è la revisione "Move to", che è la forma nella sua destinazione di arrivo.
// Se accettiamo la revisione, questa forma di revisione "Move to" scomparirà,
// e la forma di revisione "Move from" rimarrà.
ASSERT_FALSE(shapes[0]->get_IsMoveFromRevision());
ASSERT_TRUE(shapes[0]->get_IsMoveToRevision());

// Questa è la revisione "Move from", che è la forma nella sua posizione originale.
// Se accettiamo la revisione, questa forma di revisione "Move from" scomparirà,
// e la forma di revisione "Move to" rimarrà.
ASSERT_TRUE(shapes[1]->get_IsMoveFromRevision());
ASSERT_FALSE(shapes[1]->get_IsMoveToRevision());
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

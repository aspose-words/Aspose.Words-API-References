---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_IsDecorative"
linktitle: "get_IsDecorative"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_IsDecorative. Ottiene o imposta il flag che specifica se la forma è decorativa nel documento in C++."
type: docs
weight: 25000
url: /it/cpp/aspose.words.drawing/shapebase/get_isdecorative/
---
## ShapeBase::get_IsDecorative method


Ottiene o imposta il flag che specifica se la forma è decorativa nel documento.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDecorative()
```


## Esempi



Mostra come impostare che la forma sia decorativa.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Decorative shapes.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(shape->get_IsDecorative());

// Se \"AlternativeText\" non è vuoto, la forma non può essere decorativa.
// Ecco perché il nostro valore è cambiato in 'false'.
shape->set_AlternativeText(u"Alternative text.");
ASSERT_FALSE(shape->get_IsDecorative());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
// Crea una nuova forma come decorativa.
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_IsDecorative(true);

doc->Save(get_ArtifactsDir() + u"Shape.IsDecorative.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

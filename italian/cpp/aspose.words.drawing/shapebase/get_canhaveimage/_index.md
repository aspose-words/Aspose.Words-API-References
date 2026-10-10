---
title: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage metodo"
linktitle: "get_CanHaveImage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage metodo. Restituisce true se il tipo di forma consente alla forma di avere un'immagine in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.drawing/shapebase/get_canhaveimage/
---
## ShapeBase::get_CanHaveImage method


Restituisce **true** se il tipo di forma consente alla forma di avere un'immagine.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_CanHaveImage()
```

## Note


Sebbene Microsoft Word abbia un tipo di forma speciale per le immagini, sembra che nei documenti Microsoft Word qualsiasi forma, eccetto una forma di gruppo, possa avere un'immagine; pertanto questa proprietà restituisce **true** per tutte le forme eccetto [GroupShape](../../groupshape/).

## Esempi



Mostra come inserire e ruotare un'immagine.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una forma con un'immagine.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// Ruota l'immagine di 45 gradi in senso orario.
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

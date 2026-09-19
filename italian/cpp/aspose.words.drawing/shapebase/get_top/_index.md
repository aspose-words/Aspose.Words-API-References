---
title: "Aspose::Words::Drawing::ShapeBase::get_Top metodo"
linktitle: "get_Top"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Top metodo. Ottiene o imposta la posizione del bordo superiore del blocco contenitore della forma in C++."
type: docs
weight: 52000
url: /it/cpp/aspose.words.drawing/shapebase/get_top/
---
## ShapeBase::get_Top method


Ottiene o imposta la posizione del bordo superiore del blocco contenitore della forma.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Top()
```

## Note


Per una forma di livello superiore, il valore è in punti e relativo all'ancora della forma.

Per le forme in un gruppo, il valore è nello spazio delle coordinate e nelle unità del gruppo genitore.

Il valore predefinito è 0.

Ha effetto solo per le forme flottanti.

## Esempi



Mostra come inserire un'immagine flottante e specificarne la posizione e le dimensioni.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Configura la proprietà "RelativeHorizontalPosition" della forma per trattare il valore della proprietà "Left"
// come distanza orizzontale della forma, in punti, dal lato sinistro della pagina.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Imposta la distanza orizzontale della forma dal lato sinistro della pagina a 100.
shape->set_Left(100);

// Usa la proprietà "RelativeVerticalPosition" in modo simile per posizionare la forma 80pt sotto la parte superiore della pagina.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Imposta l'altezza della forma, che scalerà automaticamente la larghezza per preservare le dimensioni.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// Le proprietà "Bottom" e "Right" contengono i bordi inferiore e destro dell'immagine.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

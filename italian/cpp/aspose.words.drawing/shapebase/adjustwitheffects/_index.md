---
title: "Aspose::Words::Drawing::ShapeBase::AdjustWithEffects metodo"
linktitle: "AdjustWithEffects"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::AdjustWithEffects metodo. Aggiunge al rettangolo di origine i valori dell'estensione dell'effetto e restituisce il rettangolo finale in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing/shapebase/adjustwitheffects/
---
## ShapeBase::AdjustWithEffects method


Aggiunge al rettangolo di origine i valori dell'estensione dell'effetto e restituisce il rettangolo finale.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::AdjustWithEffects(System::Drawing::RectangleF source)
```


## Esempi



Mostra come verificare come i limiti di una forma siano influenzati dagli effetti della forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape shadow effect.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Le due forme sono identiche in termini di dimensioni e tipo di forma.
ASPOSE_ASSERT_EQ(shapes[0]->get_Width(), shapes[1]->get_Width());
ASPOSE_ASSERT_EQ(shapes[0]->get_Height(), shapes[1]->get_Height());
ASSERT_EQ(shapes[0]->get_ShapeType(), shapes[1]->get_ShapeType());

// La prima forma non ha effetti, mentre la seconda ha un'ombra e un contorno spesso.
// Questi effetti rendono la dimensione della silhouette della seconda forma più grande di quella della prima.
// Anche se le dimensioni del rettangolo compaiono quando facciamo clic su queste forme in Microsoft Word,
// i limiti esterni visibili della seconda forma sono influenzati dall'ombra e dal contorno e quindi sono più grandi.
// Possiamo usare il metodo "AdjustWithEffects" per vedere la dimensione reale della forma.
ASPOSE_ASSERT_EQ(0.0, shapes[0]->get_StrokeWeight());
ASPOSE_ASSERT_EQ(20.0, shapes[1]->get_StrokeWeight());
ASSERT_FALSE(shapes[0]->get_ShadowEnabled());
ASSERT_TRUE(shapes[1]->get_ShadowEnabled());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = shapes[0];

// Crea un oggetto RectangleF, che rappresenta un rettangolo,
// che potremmo potenzialmente usare come coordinate e limiti per una forma.
System::Drawing::RectangleF rectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);

// Esegui questo metodo per ottenere le dimensioni del rettangolo aggiustate per tutti i nostri effetti di forma.
System::Drawing::RectangleF rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Poiché la forma non ha effetti che modificano il bordo, le sue dimensioni di contorno non sono influenzate.
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_Y());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Height());

// Verifica l'estensione finale della prima forma, in punti.
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Height());

shape = shapes[1];
rectangleF = System::Drawing::RectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);
rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Gli effetti della forma hanno spostato leggermente l'angolo in alto a sinistra apparente della forma.
ASPOSE_ASSERT_EQ(171.5, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(167, rectangleFOut.get_Y());

// Gli effetti hanno anche influenzato le dimensioni visibili della forma.
ASPOSE_ASSERT_EQ(1045, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1133.5, rectangleFOut.get_Height());

// Gli effetti hanno anche influenzato i limiti visibili della forma.
ASPOSE_ASSERT_EQ(-28.5, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(-33, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(192, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(280.5, shape->get_BoundsWithEffects().get_Height());
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

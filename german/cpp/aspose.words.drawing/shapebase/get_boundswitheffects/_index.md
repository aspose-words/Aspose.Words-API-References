---
title: "Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects Methode"
linktitle: "get_BoundsWithEffects"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects Methode. Gibt die endgültige Ausdehnung dieses Formobjekts nach Anwendung von Zeicheneffekten zurück. Der Wert wird in Punkten in C++ gemessen."
type: docs
weight: 11000
url: /de/cpp/aspose.words.drawing/shapebase/get_boundswitheffects/
---
## ShapeBase::get_BoundsWithEffects method


Liest die endgültige Ausdehnung, die dieses Formobjekt nach Anwendung von Zeichnungseffekten hat. Der Wert wird in Punkten gemessen.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects()
```


## Beispiele



Zeigt, wie man prüft, wie die Grenzen einer Form durch Formeffekte beeinflusst werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape shadow effect.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Die beiden Formen sind hinsichtlich Abmessungen und Formtyp identisch.
ASPOSE_ASSERT_EQ(shapes[0]->get_Width(), shapes[1]->get_Width());
ASPOSE_ASSERT_EQ(shapes[0]->get_Height(), shapes[1]->get_Height());
ASSERT_EQ(shapes[0]->get_ShapeType(), shapes[1]->get_ShapeType());

// Die erste Form hat keine Effekte, und die zweite hat einen Schatten und eine dicke Kontur.
// Diese Effekte vergrößern die Silhouette der zweiten Form im Vergleich zur ersten.
// Obwohl die Größe des Rechtecks angezeigt wird, wenn wir in Microsoft Word auf diese Formen klicken,
// sind die sichtbaren äußeren Begrenzungen der zweiten Form durch den Schatten und die Kontur beeinflusst und daher größer.
// Wir können die Methode "AdjustWithEffects" verwenden, um die tatsächliche Größe der Form zu sehen.
ASPOSE_ASSERT_EQ(0.0, shapes[0]->get_StrokeWeight());
ASPOSE_ASSERT_EQ(20.0, shapes[1]->get_StrokeWeight());
ASSERT_FALSE(shapes[0]->get_ShadowEnabled());
ASSERT_TRUE(shapes[1]->get_ShadowEnabled());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = shapes[0];

// Erstellen Sie ein RectangleF-Objekt, das ein Rechteck darstellt,
// das wir potenziell als Koordinaten und Begrenzungen für eine Form verwenden könnten.
System::Drawing::RectangleF rectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);

// Führen Sie diese Methode aus, um die Größe des Rechtecks zu erhalten, die an alle Formeffekte angepasst ist.
System::Drawing::RectangleF rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Da die Form keine randverändernden Effekte hat, bleiben ihre Begrenzungsmaße unverändert.
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_Y());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Height());

// Überprüfen Sie die endgültige Ausdehnung der ersten Form in Punkten.
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Height());

shape = shapes[1];
rectangleF = System::Drawing::RectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);
rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Die Formeffekte haben die scheinbare obere linke Ecke der Form leicht verschoben.
ASPOSE_ASSERT_EQ(171.5, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(167, rectangleFOut.get_Y());

// Die Effekte haben zudem die sichtbaren Abmessungen der Form beeinflusst.
ASPOSE_ASSERT_EQ(1045, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1133.5, rectangleFOut.get_Height());

// Die Effekte haben zudem die sichtbaren Begrenzungen der Form beeinflusst.
ASPOSE_ASSERT_EQ(-28.5, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(-33, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(192, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(280.5, shape->get_BoundsWithEffects().get_Height());
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

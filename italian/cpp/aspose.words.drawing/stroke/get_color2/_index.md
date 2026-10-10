---
title: "Aspose::Words::Drawing::Stroke::get_Color2 metodo"
linktitle: "get_Color2"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Stroke::get_Color2 metodo. Definisce un secondo colore per un tratto in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.drawing/stroke/get_color2/
---
## Stroke::get_Color2 method


Definisce un secondo colore per un tratto.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Stroke::get_Color2()
```

## Note


Il valore predefinito per un [Shape](../../shape/) è **White**.

## Esempi



Mostra come elaborare le caratteristiche del tratto della forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();

// I tratti possono avere due colori, che vengono utilizzati per creare un motivo definito da dati immagine a due toni.
// I tratti con un solo colore non utilizzano la proprietà Color2.
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 128, 0, 0), stroke->get_Color());
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 255, 0), stroke->get_Color2());

ASSERT_FALSE(System::TestTools::IsNull(stroke->get_ImageBytes()));
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Drawing.StrokePattern.png", stroke->get_ImageBytes());
```

## Vedi anche

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

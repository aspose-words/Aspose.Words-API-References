---
title: "Aspose::Words::Drawing::Stroke::get_ImageBytes metodo"
linktitle: "get_ImageBytes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Stroke::get_ImageBytes metodo. Definisce l'immagine per un riempimento con immagine o motivo di tratto in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.drawing/stroke/get_imagebytes/
---
## Stroke::get_ImageBytes method


Definisce l'immagine per un riempimento con immagine o motivo del tratto.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::Stroke::get_ImageBytes()
```


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

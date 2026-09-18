---
title: "Methode Aspose::Words::ImageWatermarkOptions::get_Scale"
linktitle: "get_Scale"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Methode Aspose::Words::ImageWatermarkOptions::get_Scale. Gibt den Skalierungsfaktor zurück oder legt ihn fest, ausgedrückt als Bruchteil des Bildes. Der Standardwert ist 0 – auto in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/imagewatermarkoptions/get_scale/
---
## ImageWatermarkOptions::get_Scale method


Liest oder setzt den Skalierungsfaktor, ausgedrückt als Bruchteil des Bildes. Der Standardwert ist 0 – automatisch.

```cpp
double Aspose::Words::ImageWatermarkOptions::get_Scale() const
```

## Hinweise


Gültige Werte liegen im Bereich von 0 bis 65,5 inklusive.

Automatisches Skalieren bedeutet, dass das Wasserzeichen auf seine maximale Breite und maximale Höhe relativ zu den Seitenrändern skaliert wird.

## Beispiele



Zeigt, wie man ein Wasserzeichen aus einem Bild im lokalen Dateisystem erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ändern Sie das Aussehen des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt,
// und übergeben Sie es beim Erstellen eines Wasserzeichens aus einer Bilddatei.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Wir haben verschiedene Optionen, um ein Bild einzufügen.
// Verwenden Sie eine der folgenden Methoden, um ein Bildwasserzeichen hinzuzufügen.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Siehe auch

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

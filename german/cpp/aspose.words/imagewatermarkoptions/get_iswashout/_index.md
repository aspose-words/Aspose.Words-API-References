---
title: "Methode Aspose::Words::ImageWatermarkOptions::get_IsWashout"
linktitle: "get_IsWashout"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Methode Aspose::Words::ImageWatermarkOptions::get_IsWashout. Gibt einen booleschen Wert zurück oder legt ihn fest, der für den Auswascheffekt des Wasserzeichens verantwortlich ist. Der Standardwert ist true in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/imagewatermarkoptions/get_iswashout/
---
## ImageWatermarkOptions::get_IsWashout method


Liest oder setzt einen booleschen Wert, der für den Auswascheffekt des Wasserzeichens verantwortlich ist. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::ImageWatermarkOptions::get_IsWashout() const
```


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

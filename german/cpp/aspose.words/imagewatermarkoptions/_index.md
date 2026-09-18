---
title: "Aspose::Words::ImageWatermarkOptions Klasse"
linktitle: "ImageWatermarkOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImageWatermarkOptions Klasse. Enthält Optionen, die beim Hinzufügen eines Wasserzeichens mit Bild angegeben werden können. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 34000
url: /de/cpp/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class


Enthält Optionen, die beim Hinzufügen eines Bild-Wasserzeichens angegeben werden können. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class ImageWatermarkOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_IsWashout](./get_iswashout/)() const | Liest oder setzt einen booleschen Wert, der für den Auswascheffekt des Wasserzeichens verantwortlich ist. Der Standardwert ist **true**. |
| [get_Scale](./get_scale/)() const | Liest oder setzt den Skalierungsfaktor, ausgedrückt als Bruchteil des Bildes. Der Standardwert ist 0 – automatisch. |
| [GetType](./gettype/)() const override |  |
| [ImageWatermarkOptions](./imagewatermarkoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsWashout](./set_iswashout/)(bool) | Setter für [Aspose::Words::ImageWatermarkOptions::get_IsWashout](./get_iswashout/). |
| [set_Scale](./set_scale/)(double) | Setter für [Aspose::Words::ImageWatermarkOptions::get_Scale](./get_scale/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

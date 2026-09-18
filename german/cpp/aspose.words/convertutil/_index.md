---
title: "Aspose::Words::ConvertUtil class"
linktitle: "ConvertUtil"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ConvertUtil Klasse. Stellt Hilfsfunktionen zum Konvertieren zwischen verschiedenen Maßeinheiten bereit. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 19000
url: /de/cpp/aspose.words/convertutil/
---
## ConvertUtil class


Stellt Hilfsfunktionen zum Konvertieren zwischen verschiedenen Maßeinheiten bereit. Weitere Informationen finden Sie im Dokumentationsartikel [Convert Between Measurement Units](https://docs.aspose.com/words/cpp/convert-between-measurement-units/).

```cpp
class ConvertUtil
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ConvertUtil](./convertutil/)() |  |
| static [InchToPoint](./inchtopoint/)(double) | Konvertiert Zoll in Punkte. |
| static [MillimeterToPoint](./millimetertopoint/)(double) | Konvertiert Millimeter in Punkte. |
| static [PixelToNewDpi](./pixeltonewdpi/)(double, double, double) | Konvertiert Pixel von einer Auflösung in eine andere. |
| static [PixelToPoint](./pixeltopoint/)(double) | Konvertiert Pixel bei 96 DPI in Punkte. |
| static [PixelToPoint](./pixeltopoint/)(double, double) | Konvertiert Pixel bei der angegebenen Pixeldichte in Punkte. |
| static [PointToInch](./pointtoinch/)(double) | Konvertiert Punkte in Zoll. |
| static [PointToPixel](./pointtopixel/)(double) | Konvertiert Punkte bei 96 DPI in Pixel. |
| static [PointToPixel](./pointtopixel/)(double, double) | Konvertiert Punkte bei der angegebenen Pixeldichte in Pixel. |

## Beispiele



Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```


Zeigt, wie man Seiteneigenschaften in Zoll angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Der \"Page Setup\" eines Abschnitts definiert die Größe der Seitenränder in Punkten.
// Wir können auch die Klasse \"ConvertUtil\" verwenden, um eine vertrautere Maßeinheit zu nutzen,
// wie Zoll beim Definieren von Grenzen.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(2.0));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(2.5));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));

// Ein Zoll entspricht 72 Punkten.
ASPOSE_ASSERT_EQ(72.0, Aspose::Words::ConvertUtil::InchToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToInch(72));

// Fügen Sie Inhalt hinzu, um die neuen Ränder zu demonstrieren.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} inches from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} inches from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} inches from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} inches from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndInches.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

---
title: "Aspose::Words::ConvertUtil::PointToPixel Methode"
linktitle: "PointToPixel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ConvertUtil::PointToPixel Methode. Konvertiert Punkte zu Pixeln bei 96 dpi in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words/convertutil/pointtopixel/
---
## ConvertUtil::PointToPixel(double) method


Konvertiert Punkte bei 96 DPI in Pixel.

```cpp
static double Aspose::Words::ConvertUtil::PointToPixel(double points)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Punkte | double | Der zu konvertierende Wert. |

## Beispiele



Zeigt, wie man Seiteneigenschaften in Pixeln angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Der \"Page Setup\" eines Abschnitts definiert die Größe der Seitenränder in Punkten.
// Wir können auch die "ConvertUtil"-Klasse verwenden, um eine andere Maßeinheit zu nutzen,
// wie Pixel beim Definieren von Grenzen.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::PixelToPoint(200));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::PixelToPoint(225));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::PixelToPoint(125));

// Ein Pixel entspricht 0,75 Punkten.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToPixel(0.75));

// Der standardmäßig verwendete DPI-Wert ist 96.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1, 96));

// Fügen Sie Inhalt hinzu, um die neuen Ränder zu demonstrieren.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} pixels from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} pixels from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} pixels from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} pixels from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixels.docx");
```

## Siehe auch

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## ConvertUtil::PointToPixel(double, double) method


Konvertiert Punkte bei der angegebenen Pixeldichte in Pixel.

```cpp
static double Aspose::Words::ConvertUtil::PointToPixel(double points, double resolution)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Punkte | double | Der zu konvertierende Wert. |
| Auflösung | double | Die DPI (dots per inch)-Auflösung. |

## Beispiele



Zeigt, wie man Punkte in Pixel mit Standard- und benutzerdefinierter Auflösung umwandelt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Definieren Sie die Größe des oberen Randes dieses Abschnitts in Pixeln, basierend auf einer benutzerdefinierten DPI.
const double myDpi = 192;

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100, myDpi));

ASSERT_NEAR(37.5, pageSetup->get_TopMargin(), 0.01);

// Bei der Standard-DPI von 96 entspricht ein Pixel 0,75 Punkten.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));

builder->Writeln(System::String::Format(u"This Text is {0} points/{1} ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + System::String::Format(u"pixels (at a DPI of {0}) from the top of the page.", myDpi));

// Legen Sie eine neue DPI fest und passen Sie den Wert des oberen Randes entsprechend an.
const double newDpi = 300;
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToNewDpi(pageSetup->get_TopMargin(), myDpi, newDpi));
ASSERT_NEAR(59.0, pageSetup->get_TopMargin(), 0.01);

builder->Writeln(System::String::Format(u"At a DPI of {0}, the text is now {1} points/{2} ", newDpi, pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + u"pixels from the top of the page.");

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixelsDpi.docx");
```

## Siehe auch

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

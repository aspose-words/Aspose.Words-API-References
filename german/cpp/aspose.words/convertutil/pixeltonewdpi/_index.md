---
title: "Aspose::Words::ConvertUtil::PixelToNewDpi Methode"
linktitle: "PixelToNewDpi"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ConvertUtil::PixelToNewDpi Methode. Konvertiert Pixel von einer Auflösung in eine andere in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil::PixelToNewDpi method


Konvertiert Pixel von einer Auflösung in eine andere.

```cpp
static int32_t Aspose::Words::ConvertUtil::PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Pixel | double | Der zu konvertierende Wert. |
| oldDpi | double | Die aktuelle DPI (dots per inch)-Auflösung. |
| newDpi | double | Die neue DPI (dots per inch)-Auflösung. |

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

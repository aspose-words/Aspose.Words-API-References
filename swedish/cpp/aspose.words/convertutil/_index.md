---
title: "Aspose::Words::ConvertUtil class"
linktitle: "ConvertUtil"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ConvertUtil-klass. Tillhandahåller hjälpfunktioner för att konvertera mellan olika måttenheter. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words/convertutil/
---
## ConvertUtil class


Tillhandahåller hjälpfunktioner för att konvertera mellan olika måttenheter. För att läsa mer, besök dokumentationsartikeln [Konvertera mellan måttenheter](https://docs.aspose.com/words/cpp/convert-between-measurement-units/).

```cpp
class ConvertUtil
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ConvertUtil](./convertutil/)() |  |
| static [InchToPoint](./inchtopoint/)(double) | Konverterar tum till punkter. |
| static [MillimeterToPoint](./millimetertopoint/)(double) | Konverterar millimeter till punkter. |
| static [PixelToNewDpi](./pixeltonewdpi/)(double, double, double) | Konverterar pixlar från en upplösning till en annan. |
| static [PixelToPoint](./pixeltopoint/)(double) | Konverterar pixlar till punkter vid 96 dpi. |
| static [PixelToPoint](./pixeltopoint/)(double, double) | Konverterar pixlar till punkter vid den angivna pixelupplösningen. |
| static [PointToInch](./pointtoinch/)(double) | Konverterar punkter till tum. |
| static [PointToPixel](./pointtopixel/)(double) | Konverterar punkter till pixlar vid 96 dpi. |
| static [PointToPixel](./pointtopixel/)(double, double) | Konverterar punkter till pixlar vid den angivna pixelupplösningen. |

## Exempel



Visar hur man justerar papperstorlek, orientering, marginaler samt andra inställningar för ett avsnitt.
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


Visar hur man specificerar sidegenskaper i tum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ett avsnitts "Page Setup" definierar storleken på sidmarginalerna i punkter.
// Vi kan också använda "ConvertUtil"-klassen för att använda en mer bekant måttenhet,
// såsom tum när man definierar gränser.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(2.0));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(2.5));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));

// En tum är 72 punkter.
ASPOSE_ASSERT_EQ(72.0, Aspose::Words::ConvertUtil::InchToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToInch(72));

// Lägg till innehåll för att demonstrera de nya marginalerna.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} inches from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} inches from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} inches from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} inches from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndInches.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

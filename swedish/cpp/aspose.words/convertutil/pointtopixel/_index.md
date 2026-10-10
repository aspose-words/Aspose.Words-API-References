---
title: "Aspose::Words::ConvertUtil::PointToPixel metod"
linktitle: "PointToPixel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ConvertUtil::PointToPixel metod. Konverterar punkter till pixlar vid 96 dpi i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/convertutil/pointtopixel/
---
## ConvertUtil::PointToPixel(double) method


Konverterar punkter till pixlar vid 96 dpi.

```cpp
static double Aspose::Words::ConvertUtil::PointToPixel(double points)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| punkter | double | Värdet att konvertera. |

## Exempel



Visar hur man specificerar sidegenskaper i pixlar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ett avsnitts "Page Setup" definierar storleken på sidmarginalerna i punkter.
// Vi kan också använda klassen "ConvertUtil" för att använda en annan mätenhet,
// såsom pixlar när man definierar gränser.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::PixelToPoint(200));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::PixelToPoint(225));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::PixelToPoint(125));

// En pixel är 0,75 punkter.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToPixel(0.75));

// Standard‑DPI‑värdet som används är 96.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1, 96));

// Lägg till innehåll för att demonstrera de nya marginalerna.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} pixels from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} pixels from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} pixels from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} pixels from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixels.docx");
```

## Se även

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## ConvertUtil::PointToPixel(double, double) method


Konverterar punkter till pixlar vid den angivna pixelupplösningen.

```cpp
static double Aspose::Words::ConvertUtil::PointToPixel(double points, double resolution)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| punkter | double | Värdet att konvertera. |
| upplösning | double | DPI‑upplösningen (dots per inch). |

## Exempel



Visar hur man använder konvertering av punkter till pixlar med standard- och anpassad upplösning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Definiera storleken på avsnittets övre marginal i pixlar, enligt en anpassad DPI.
const double myDpi = 192;

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100, myDpi));

ASSERT_NEAR(37.5, pageSetup->get_TopMargin(), 0.01);

// Vid standard‑DPI på 96 är en pixel 0,75 punkter.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));

builder->Writeln(System::String::Format(u"This Text is {0} points/{1} ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + System::String::Format(u"pixels (at a DPI of {0}) from the top of the page.", myDpi));

// Ställ in en ny DPI och justera värdet för den övre marginalen därefter.
const double newDpi = 300;
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToNewDpi(pageSetup->get_TopMargin(), myDpi, newDpi));
ASSERT_NEAR(59.0, pageSetup->get_TopMargin(), 0.01);

builder->Writeln(System::String::Format(u"At a DPI of {0}, the text is now {1} points/{2} ", newDpi, pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + u"pixels from the top of the page.");

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixelsDpi.docx");
```

## Se även

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

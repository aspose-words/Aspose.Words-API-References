---
title: "Aspose::Words::ConvertUtil::MillimeterToPoint metod"
linktitle: "MillimeterToPoint"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ConvertUtil::MillimeterToPoint metod. Konverterar millimeter till punkter i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil::MillimeterToPoint method


Konverterar millimeter till punkter.

```cpp
static double Aspose::Words::ConvertUtil::MillimeterToPoint(double millimeters)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| millimeter | double | Värdet att konvertera. |

## Exempel



Visar hur man anger sidinställningar i millimeter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ett avsnitts "Page Setup" definierar storleken på sidmarginalerna i punkter.
// Vi kan också använda "ConvertUtil"-klassen för att använda en mer bekant måttenhet,
// såsom millimeter när man definierar gränser.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(30));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(50));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(80));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(40));

// En centimeter är ungefär 28,3 punkter.
ASSERT_NEAR(28.34, Aspose::Words::ConvertUtil::MillimeterToPoint(10), 0.01);

// Lägg till innehåll för att demonstrera de nya marginalerna.
builder->Writeln(System::String::Format(u"This Text is {0} points from the left, ", pageSetup->get_LeftMargin()) + System::String::Format(u"{0} points from the right, ", pageSetup->get_RightMargin()) + System::String::Format(u"{0} points from the top, ", pageSetup->get_TopMargin()) + System::String::Format(u"and {0} points from the bottom of the page.", pageSetup->get_BottomMargin()));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndMillimeters.docx");
```

## Se även

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

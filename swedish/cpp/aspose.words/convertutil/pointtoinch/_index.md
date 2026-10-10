---
title: "Aspose::Words::ConvertUtil::PointToInch metod"
linktitle: "PointToInch"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ConvertUtil::PointToInch metod. Konverterar punkter till tum i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil::PointToInch method


Konverterar punkter till tum.

```cpp
static double Aspose::Words::ConvertUtil::PointToInch(double points)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| punkter | double | Värdet att konvertera. |

## Exempel



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

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

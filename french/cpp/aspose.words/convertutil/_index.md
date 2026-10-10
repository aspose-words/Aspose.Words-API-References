---
title: "Aspose::Words::ConvertUtil class"
linktitle: "ConvertUtil"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ConvertUtil class. Fournit des fonctions d'aide pour convertir entre différentes unités de mesure. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words/convertutil/
---
## ConvertUtil class


Fournit des fonctions d'aide pour convertir entre différentes unités de mesure. Pour en savoir plus, consultez l'article de documentation [Convert Between Measurement Units](https://docs.aspose.com/words/cpp/convert-between-measurement-units/).

```cpp
class ConvertUtil
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ConvertUtil](./convertutil/)() |  |
| static [InchToPoint](./inchtopoint/)(double) | Convertit les pouces en points. |
| static [MillimeterToPoint](./millimetertopoint/)(double) | Convertit les millimètres en points. |
| static [PixelToNewDpi](./pixeltonewdpi/)(double, double, double) | Convertit les pixels d'une résolution à une autre. |
| static [PixelToPoint](./pixeltopoint/)(double) | Convertit les pixels en points à 96 dpi. |
| static [PixelToPoint](./pixeltopoint/)(double, double) | Convertit les pixels en points à la résolution de pixel spécifiée. |
| static [PointToInch](./pointtoinch/)(double) | Convertit les points en pouces. |
| static [PointToPixel](./pointtopixel/)(double) | Convertit les points en pixels à 96 dpi. |
| static [PointToPixel](./pointtopixel/)(double, double) | Convertit les points en pixels à la résolution de pixel spécifiée. |

## Exemples



Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.
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


Montre comment spécifier les propriétés de page en pouces.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Le "Page Setup" d'une section définit la taille des marges de la page en points.
// Nous pouvons également utiliser la classe "ConvertUtil" pour employer une unité de mesure plus familière,
// comme les pouces lors de la définition des limites.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(2.0));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(2.5));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));

// Un pouce vaut 72 points.
ASPOSE_ASSERT_EQ(72.0, Aspose::Words::ConvertUtil::InchToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToInch(72));

// Ajoutez du contenu pour démontrer les nouvelles marges.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} inches from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} inches from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} inches from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} inches from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndInches.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

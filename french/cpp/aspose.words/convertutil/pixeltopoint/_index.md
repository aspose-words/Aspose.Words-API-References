---
title: "Aspose::Words::ConvertUtil::PixelToPoint méthode"
linktitle: "PixelToPoint"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ConvertUtil::PixelToPoint méthode. Convertit les pixels en points à 96 dpi en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/convertutil/pixeltopoint/
---
## ConvertUtil::PixelToPoint(double) method


Convertit les pixels en points à 96 dpi.

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| pixels | double | La valeur à convertir. |

## Exemples



Montre comment spécifier les propriétés de page en pixels.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Le "Page Setup" d'une section définit la taille des marges de la page en points.
// Nous pouvons également utiliser la classe "ConvertUtil" pour utiliser une unité de mesure différente,
// comme les pixels lors de la définition des limites.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::PixelToPoint(200));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::PixelToPoint(225));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::PixelToPoint(125));

// Un pixel vaut 0,75 point.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToPixel(0.75));

// La valeur DPI par défaut utilisée est 96.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1, 96));

// Ajoutez du contenu pour démontrer les nouvelles marges.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} pixels from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} pixels from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} pixels from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} pixels from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixels.docx");
```

## Voir aussi

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## ConvertUtil::PixelToPoint(double, double) method


Convertit les pixels en points à la résolution de pixel spécifiée.

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels, double resolution)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| pixels | double | La valeur à convertir. |
| résolution | double | La résolution dpi (points par pouce). |

## Exemples



Montre comment convertir des points en pixels avec une résolution par défaut et personnalisée.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez la taille de la marge supérieure de cette section en pixels, selon un DPI personnalisé.
const double myDpi = 192;

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100, myDpi));

ASSERT_NEAR(37.5, pageSetup->get_TopMargin(), 0.01);

// Avec le DPI par défaut de 96, un pixel vaut 0,75 point.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));

builder->Writeln(System::String::Format(u"This Text is {0} points/{1} ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + System::String::Format(u"pixels (at a DPI of {0}) from the top of the page.", myDpi));

// Définissez un nouveau DPI et ajustez la valeur de la marge supérieure en conséquence.
const double newDpi = 300;
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToNewDpi(pageSetup->get_TopMargin(), myDpi, newDpi));
ASSERT_NEAR(59.0, pageSetup->get_TopMargin(), 0.01);

builder->Writeln(System::String::Format(u"At a DPI of {0}, the text is now {1} points/{2} ", newDpi, pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + u"pixels from the top of the page.");

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixelsDpi.docx");
```

## Voir aussi

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

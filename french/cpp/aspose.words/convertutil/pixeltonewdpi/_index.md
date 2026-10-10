---
title: "Aspose::Words::ConvertUtil::PixelToNewDpi méthode"
linktitle: "PixelToNewDpi"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ConvertUtil::PixelToNewDpi méthode. Convertit les pixels d’une résolution à une autre en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil::PixelToNewDpi method


Convertit les pixels d'une résolution à une autre.

```cpp
static int32_t Aspose::Words::ConvertUtil::PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| pixels | double | La valeur à convertir. |
| oldDpi | double | La résolution dpi actuelle (points par pouce). |
| newDpi | double | La nouvelle résolution dpi (points par pouce). |

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

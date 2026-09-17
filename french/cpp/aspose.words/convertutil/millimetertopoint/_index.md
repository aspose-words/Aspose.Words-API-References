---
title: "Aspose::Words::ConvertUtil::MillimeterToPoint méthode"
linktitle: "MillimeterToPoint"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ConvertUtil::MillimeterToPoint méthode. Convertit les millimètres en points en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil::MillimeterToPoint method


Convertit les millimètres en points.

```cpp
static double Aspose::Words::ConvertUtil::MillimeterToPoint(double millimeters)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| millimètres | double | La valeur à convertir. |

## Exemples



Montre comment spécifier les propriétés de page en millimètres.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Le "Page Setup" d'une section définit la taille des marges de la page en points.
// Nous pouvons également utiliser la classe "ConvertUtil" pour employer une unité de mesure plus familière,
// comme les millimètres lors de la définition des limites.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(30));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(50));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(80));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(40));

// Un centimètre vaut environ 28,3 points.
ASSERT_NEAR(28.34, Aspose::Words::ConvertUtil::MillimeterToPoint(10), 0.01);

// Ajoutez du contenu pour démontrer les nouvelles marges.
builder->Writeln(System::String::Format(u"This Text is {0} points from the left, ", pageSetup->get_LeftMargin()) + System::String::Format(u"{0} points from the right, ", pageSetup->get_RightMargin()) + System::String::Format(u"{0} points from the top, ", pageSetup->get_TopMargin()) + System::String::Format(u"and {0} points from the bottom of the page.", pageSetup->get_BottomMargin()));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndMillimeters.docx");
```

## Voir aussi

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

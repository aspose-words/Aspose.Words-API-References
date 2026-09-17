---
title: "Aspose::Words::ConvertUtil::PointToInch méthode"
linktitle: "PointToInch"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ConvertUtil::PointToInch méthode. Convertit les points en pouces en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil::PointToInch method


Convertit les points en pouces.

```cpp
static double Aspose::Words::ConvertUtil::PointToInch(double points)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| points | double | La valeur à convertir. |

## Exemples



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

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

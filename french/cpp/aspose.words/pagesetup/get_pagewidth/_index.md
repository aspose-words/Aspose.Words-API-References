---
title: "Aspose::Words::PageSetup::get_PageWidth méthode"
linktitle: "get_PageWidth"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::PageSetup::get_PageWidth. Retourne ou définit la largeur de la page en points en C++."
type: docs
weight: 36000
url: /fr/cpp/aspose.words/pagesetup/get_pagewidth/
---
## PageSetup::get_PageWidth method


Renvoie ou définit la largeur de la page en points.

```cpp
double Aspose::Words::PageSetup::get_PageWidth()
```


## Exemples



Montre comment insérer une image et l'utiliser comme filigrane.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez l'image dans l'en-tête afin qu'elle soit visible sur chaque page.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Placez l'image au centre de la page.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```


Montre comment insérer une image flottante et spécifier sa position et sa taille.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Configurez la propriété "RelativeHorizontalPosition" de la forme pour traiter la valeur de la propriété "Left"
// comme la distance horizontale de la forme, en points, depuis le côté gauche de la page.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Définissez la distance horizontale de la forme depuis le côté gauche de la page à 100.
shape->set_Left(100);

// Utilisez la propriété "RelativeVerticalPosition" de manière similaire pour positionner la forme à 80 pt sous le haut de la page.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Définissez la hauteur de la forme, ce qui ajustera automatiquement la largeur pour préserver les dimensions.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// Les propriétés "Bottom" et "Right" contiennent respectivement les bords inférieur et droit de l'image.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

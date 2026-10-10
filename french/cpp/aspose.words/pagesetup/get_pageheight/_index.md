---
title: "Méthode Aspose::Words::PageSetup::get_PageHeight"
linktitle: "get_PageHeight"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::PageSetup::get_PageHeight. Retourne ou définit la hauteur de la page en points en C++."
type: docs
weight: 33000
url: /fr/cpp/aspose.words/pagesetup/get_pageheight/
---
## PageSetup::get_PageHeight method


Renvoie ou définit la hauteur de la page en points.

```cpp
double Aspose::Words::PageSetup::get_PageHeight()
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

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

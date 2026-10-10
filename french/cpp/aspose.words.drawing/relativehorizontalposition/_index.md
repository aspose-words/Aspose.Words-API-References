---
title: "Aspose::Words::Drawing::RelativeHorizontalPosition enum"
linktitle: "RelativeHorizontalPosition"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::RelativeHorizontalPosition enum. Spécifie à quoi la position horizontale d'une forme ou d'un cadre de texte est relative en C++."
type: docs
weight: 33000
url: /fr/cpp/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enum


Spécifie par rapport à quoi la position horizontale d’une forme ou d’un cadre de texte est relative.

```cpp
enum class RelativeHorizontalPosition
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Marge | 0 | Spécifie que le positionnement horizontal doit être relatif aux marges de la page. |
| Page | 1 | L'objet est positionné par rapport au bord gauche de la page. |
| Colonne | 2 | L'objet est positionné par rapport au côté gauche de la colonne. |
| Character | 3 | L'objet est positionné par rapport au côté gauche du paragraphe. |
| LeftMargin | 4 | Spécifie que le positionnement horizontal doit être relatif à la marge gauche de la page. |
| RightMargin | 5 | Spécifie que le positionnement horizontal doit être relatif à la marge droite de la page. |
| InsideMargin | 6 | Spécifie que le positionnement horizontal doit être relatif à la marge intérieure de la page actuelle (la marge gauche sur les pages impaires, droite sur les pages paires). |
| OutsideMargin | 7 | Spécifie que le positionnement horizontal doit être relatif à la marge extérieure de la page actuelle (la marge droite sur les pages impaires, gauche sur les pages paires). |
| Default | n/a | La valeur par défaut est [Column](./). |


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


Montre comment insérer une image flottante au centre d'une page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une image flottante qui apparaîtra derrière le texte qui se chevauche et alignez‑la au centre de la page.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)

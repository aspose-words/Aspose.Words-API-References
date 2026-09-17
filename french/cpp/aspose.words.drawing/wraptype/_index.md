---
title: "Aspose::Words::Drawing::WrapType enum"
linktitle: "WrapType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::WrapType enum. Spécifie comment le texte est enveloppé autour d'une forme ou d'une image en C++."
type: docs
weight: 45000
url: /fr/cpp/aspose.words.drawing/wraptype/
---
## WrapType enum


Spécifie comment le texte s’enroule autour d’une forme ou d’une image.

```cpp
enum class WrapType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 3 | Pas d'enveloppement du texte autour de la forme. La forme est placée derrière ou devant le texte. |
| Inline | 0 | La forme reste sur la même couche que le texte et est traitée comme un caractère. |
| TopBottom | 1 | Le texte s'arrête en haut de la forme et reprend sur la ligne située sous la forme. |
| Square | 2 | Enveloppe le texte autour de tous les côtés de la boîte englobante carrée de la forme. |
| Tight | 4 | Enveloppe étroitement les bords de la forme, au lieu d'envelopper la boîte englobante. |
| Through | 5 | Identique à Tight, mais enveloppe à l'intérieur de toutes les parties de la forme qui sont ouvertes. |


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

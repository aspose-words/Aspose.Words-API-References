---
title: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter method"
linktitle: "MoveToHeaderFooter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter method. Déplace le curseur au début d'un en-tête ou d'un pied de page dans la section actuelle en C++."
type: docs
weight: 57000
url: /fr/cpp/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder::MoveToHeaderFooter method


Déplace le curseur vers le début d'un en-tête ou d'un pied de page dans la section actuelle.

```cpp
void Aspose::Words::DocumentBuilder::MoveToHeaderFooter(Aspose::Words::HeaderFooterType headerFooterType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Spécifie l'en-tête ou le pied de page vers lequel se déplacer. |
## Remarques


Après avoir déplacé le curseur dans un en-tête ou un pied de page, vous pouvez utiliser le reste des méthodes de [DocumentBuilder](../) pour modifier le contenu de l'en-tête ou du pied de page.

Si vous souhaitez créer des en-têtes et pieds de page différents pour la première page, vous devez définir [DifferentFirstPageHeaderFooter](../../pagesetup/get_differentfirstpageheaderfooter/).

Si vous souhaitez créer des en-têtes et pieds de page différents pour les pages paires et impaires, vous devez définir [OddAndEvenPagesHeaderFooter](../../pagesetup/get_oddandevenpagesheaderfooter/).

Utilisez [MoveToSection()](../movetosection/) pour sortir de l'en-tête vers le texte principal.

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

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)

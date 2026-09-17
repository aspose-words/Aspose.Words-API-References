---
title: "Aspose::Words::Drawing::ImageData::get_BiLevel méthode"
linktitle: "get_BiLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ImageData::get_BiLevel méthode. Détermine si une image sera affichée en noir et blanc en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing/imagedata/get_bilevel/
---
## ImageData::get_BiLevel method


Détermine si une image sera affichée en noir et blanc.

```cpp
bool Aspose::Words::Drawing::ImageData::get_BiLevel()
```

## Remarques


La valeur par défaut est **false**.

## Exemples



Montre comment modifier les données d'image d'une forme.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
auto sourceShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

auto dstDoc = System::MakeObject<Aspose::Words::Document>();

// Importez une forme du document source et ajoutez‑la au premier paragraphe.
auto importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

// La forme importée contient une image. Nous pouvons accéder aux propriétés de l'image et aux données brutes via l'objet ImageData.
System::SharedPtr<Aspose::Words::Drawing::ImageData> imageData = importedShape->get_ImageData();
imageData->set_Title(u"Imported Image");

ASSERT_TRUE(imageData->get_HasImage());

// Si une image n'a pas de bordures, son objet ImageData définira la couleur de bordure comme vide.
ASSERT_EQ(4, imageData->get_Borders()->get_Count());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, imageData->get_Borders()->idx_get(0)->get_Color());

// Cette image ne lie pas à une autre forme ou à un fichier image dans le système de fichiers local.
ASSERT_FALSE(imageData->get_IsLink());
ASSERT_FALSE(imageData->get_IsLinkOnly());

// Les propriétés "Brightness" et "Contrast" définissent la luminosité et le contraste de l'image
// sur une échelle de 0 à 1, avec la valeur par défaut à 0,5.
imageData->set_Brightness(0.8);
imageData->set_Contrast(1.0);

// Les valeurs de luminosité et de contraste ci‑dessus ont créé une image très blanche.
// Nous pouvons sélectionner une couleur avec la propriété ChromaKey pour la remplacer par de la transparence, comme le blanc.
imageData->set_ChromaKey(System::Drawing::Color::get_White());

// Importez à nouveau la forme source et définissez l'image en monochrome.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_GrayScale(true);

// Importez à nouveau la forme source pour créer une troisième image et définissez‑la en BiLevel.
// BiLevel définit chaque pixel en noir ou blanc, selon ce qui est le plus proche de la couleur originale.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_BiLevel(true);

// Le recadrage est déterminé sur une échelle de 0-1. Recadrer un côté de 0.3
// recadrera 30% de l'image du côté recadré.
importedShape->get_ImageData()->set_CropBottom(0.3);
importedShape->get_ImageData()->set_CropLeft(0.3);
importedShape->get_ImageData()->set_CropTop(0.3);
importedShape->get_ImageData()->set_CropRight(0.3);

dstDoc->Save(get_ArtifactsDir() + u"Drawing.ImageData.docx");
```

## Voir aussi

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)

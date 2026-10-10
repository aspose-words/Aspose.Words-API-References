---
title: "Aspose::Words::Saving::ImageSaveOptions::get_Scale méthode"
linktitle: "get_Scale"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_Scale méthode. Obtient ou définit le facteur de zoom pour les images générées en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/get_scale/
---
## ImageSaveOptions::get_Scale method


Obtient ou définit le facteur de zoom des images générées.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_Scale() const
```


## Exemples



Montre comment modifier l’image pendant qu’Aspose.Words convertit un document en une image.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Lorsque nous enregistrons le document en tant qu’image, nous pouvons passer un objet SaveOptions à
// modifier l'image pendant que l'opération d'enregistrement la rend.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Nous pouvons ajuster ces propriétés pour modifier la luminosité et le contraste de l'image.
// Les deux sont sur une échelle de 0 à 1 et sont à 0,5 par défaut.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Nous pouvons ajuster la résolution horizontale et verticale avec ces propriétés.
// Cela affectera les dimensions de l'image.
// La valeur par défaut pour ces propriétés est 96,0, pour une résolution de 96 dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Nous pouvons mettre à l'échelle l'image en utilisant cette propriété. La valeur par défaut est 1,0, pour un agrandissement de 100 %.
// Nous pouvons utiliser cette propriété pour annuler toute modification des dimensions de l'image que le changement de résolution entraînerait.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```


Montre comment rendre un objet Office [Math](../../../aspose.words.math/) en un fichier image dans le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Créez un objet "ImageSaveOptions" à transmettre à la méthode "Save" du rendu de nœud pour modifier
// la façon dont il rend le nœud OfficeMath en image.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Définissez la propriété "Scale" à 5 pour rendre l'objet à cinq fois sa taille originale.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Voir aussi

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Méthode Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf"
linktitle: "get_SaveImagesAsWmf"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf. Lorsque true, toutes les images seront enregistrées au format WMF en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/rtfsaveoptions/get_saveimagesaswmf/
---
## RtfSaveOptions::get_SaveImagesAsWmf method


Lorsque **true** toutes les images seront enregistrées au format WMF.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf() const
```


## Exemples



Montre comment convertir toutes les images d’un document au format Windows Metafile lors de l’enregistrement du document au format RTF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jpeg image:");
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imageShape->get_ImageData()->get_ImageType());

builder->InsertParagraph();
builder->Writeln(u"Png image:");
imageShape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, imageShape->get_ImageData()->get_ImageType());

// Créez un objet "RtfSaveOptions" à transmettre à la méthode "Save" du document afin de modifier la façon dont nous l'enregistrons au format RTF.
auto rtfSaveOptions = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

// Définissez la propriété "SaveImagesAsWmf" sur "true" pour convertir toutes les images du document en WMF lors de son enregistrement au format RTF.
// Cela aidera des lecteurs comme WordPad à lire notre document.
// Définissez la propriété "SaveImagesAsWmf" sur "false" pour conserver le format d’origine de toutes les images du document
// lors de son enregistrement au format RTF. Cela préservera la qualité des images au détriment de la compatibilité avec les lecteurs RTF plus anciens.
rtfSaveOptions->set_SaveImagesAsWmf(saveImagesAsWmf);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"RtfSaveOptions.SaveImagesAsWmf.rtf");

System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

if (saveImagesAsWmf)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Wmf, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0)))->get_ImageData()->get_ImageType());
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Wmf, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0)))->get_ImageData()->get_ImageType());
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1)))->get_ImageData()->get_ImageType());
}
```

## Voir aussi

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

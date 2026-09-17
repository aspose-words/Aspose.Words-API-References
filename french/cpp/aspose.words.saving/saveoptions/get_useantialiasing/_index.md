---
title: "Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing méthode"
linktitle: "get_UseAntiAliasing"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing méthode. Obtient ou définit une valeur déterminant s’il faut ou non utiliser l’anti-aliasing pour le rendu en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words.saving/saveoptions/get_useantialiasing/
---
## SaveOptions::get_UseAntiAliasing method


Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage lors du rendu.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing() const
```

## Remarques


La valeur par défaut est **false**. Lorsque cette valeur est définie sur **true**, l’anti-aliasing est utilisé pour le rendu.

Cette propriété est utilisée lorsque le document est exporté vers les formats suivants : [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/). Lorsque le document est exporté vers les formats [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) ou [Mobi](../../../aspose.words/saveformat/), cette option est utilisée pour les images raster.

## Exemples



Montre comment améliorer la qualité d'un document rendu avec [SaveOptions](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```

## Voir aussi

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

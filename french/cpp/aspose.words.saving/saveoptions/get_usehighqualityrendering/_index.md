---
title: "Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering méthode"
linktitle: "get_UseHighQualityRendering"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering méthode. Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu haute qualité (c.-à-d. lents) en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words.saving/saveoptions/get_usehighqualityrendering/
---
## SaveOptions::get_UseHighQualityRendering method


Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c’est‑à‑dire lents).

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering() const
```

## Remarques


La valeur par défaut est **false**.

Cette propriété est utilisée lorsque le document est exporté vers des formats d'image : [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/).

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

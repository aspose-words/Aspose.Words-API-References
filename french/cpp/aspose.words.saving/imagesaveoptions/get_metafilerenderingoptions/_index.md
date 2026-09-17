---
title: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions méthode"
linktitle: "get_MetafileRenderingOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions méthode. Permet de spécifier comment les métafichiers sont traités dans la sortie rendue en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/get_metafilerenderingoptions/
---
## ImageSaveOptions::get_MetafileRenderingOptions method


Permet de spécifier comment les métafichiers sont traités dans la sortie rendue.

```cpp
System::SharedPtr<Aspose::Words::Saving::MetafileRenderingOptions> Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions()
```

## Remarques


Lorsque [Vector](../../metafilerenderingmode/) est spécifié, Aspose.Words rend le métafile en graphiques vectoriels en utilisant d'abord son propre moteur de rendu de métafichiers, puis rend les graphiques vectoriels dans l'image.

Lorsque [Bitmap](../../metafilerenderingmode/) est spécifié, Aspose.Words rend le métafile directement dans l'image en utilisant le moteur de rendu de métafichiers GDI+.

Le moteur de rendu de métafichiers GDI+ fonctionne plus rapidement, prend en charge presque toutes les fonctionnalités des métafichiers mais, à basse résolution, peut produire un résultat incohérent comparé au reste des graphiques vectoriels (en particulier pour le texte) sur la page. Le moteur de rendu de métafichiers d'Aspose.Words produira un résultat plus cohérent même à basse résolution, mais fonctionne plus lentement et peut rendre de manière inexacte les métafichiers complexes.

The default value for [MetafileRenderingMode](../../metafilerenderingmode/) is [Bitmap](../../metafilerenderingmode/).

## Exemples



Montre comment définir le mode de rendu lors de l’enregistrement de documents contenant des images Windows Metafile vers d’autres formats d’image.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf");

// Lorsque nous enregistrons le document en tant qu’image, nous pouvons passer un objet SaveOptions à
// détermine comment l’opération d’enregistrement traitera les Windows Metafiles dans le document.
// Si nous définissons la propriété "RenderingMode" sur "MetafileRenderingMode.Vector",
// ou "MetafileRenderingMode.VectorWithFallback", nous rendrons tous les métafichiers en tant que graphiques vectoriels.
// Si nous définissons la propriété "RenderingMode" sur "MetafileRenderingMode.Bitmap", nous rendrons tous les métafichiers sous forme de bitmap.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
options->get_MetafileRenderingOptions()->set_RenderingMode(metafileRenderingMode);
// Aspose.Words utilise GDI+ pour l’émulation des opérations raster, lorsque la valeur est définie sur true.
options->get_MetafileRenderingOptions()->set_UseGdiRasterOperationsEmulation(true);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.WindowsMetaFile.png", options);
```

## Voir aussi

* Class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

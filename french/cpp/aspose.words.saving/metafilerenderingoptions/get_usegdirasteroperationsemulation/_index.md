---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation méthode"
linktitle: "get_UseGdiRasterOperationsEmulation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation. Obtient ou définit une valeur déterminant s'il faut ou non utiliser GDI+ pour l'émulation des opérations raster en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.saving/metafilerenderingoptions/get_usegdirasteroperationsemulation/
---
## MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method


Obtient ou définit une valeur déterminant s'il faut ou non utiliser GDI+ pour l'émulation des opérations raster.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation() const
```

## Remarques


La bibliothèque Windows GDI+ peut être utilisée pour émuler les opérations raster. Elle offre une prise en charge de toutes les opérations raster comparée à l'émulation propre à Aspose.Words, mais les performances peuvent être plus lentes dans certains cas.

Lorsque cette valeur est définie sur **true**, Aspose.Words utilise GDI+ pour l'émulation des opérations raster.

Lorsque cette valeur est définie sur **false**, Aspose.Words utilise sa propre implémentation de l'émulation des opérations raster.

Cette option n'est utilisée que lorsque le fichier métas est rendu en graphiques vectoriels.

La valeur par défaut est **false**.

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

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

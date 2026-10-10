---
title: "Méthode Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements"
linktitle: "get_RasterizeTransformedElements"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements. Obtient ou définit une valeur déterminant si les éléments transformés complexes doivent être rasterisés avant l’enregistrement dans un document PCL. La valeur par défaut est true en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/pclsaveoptions/get_rasterizetransformedelements/
---
## PclSaveOptions::get_RasterizeTransformedElements method


Obtient ou définit une valeur déterminant si les éléments transformés complexes doivent être rasterisés avant l'enregistrement du document PCL. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements() const
```


## Exemples



Montre comment rasteriser des éléments complexes lors de l'enregistrement d'un document au format PCL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(get_ArtifactsDir() + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

## Voir aussi

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

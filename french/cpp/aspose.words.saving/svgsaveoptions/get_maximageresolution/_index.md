---
title: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution méthode"
linktitle: "get_MaxImageResolution"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution méthode. Obtient ou définit une valeur en pixels par pouce qui limite la résolution des images raster exportées. La valeur par défaut est zéro en C++."
type: docs
weight: 4500
url: /fr/cpp/aspose.words.saving/svgsaveoptions/get_maximageresolution/
---
## SvgSaveOptions::get_MaxImageResolution method


Obtient ou définit une valeur en pixels par pouce qui limite la résolution des images raster exportées. La valeur par défaut est zéro.

```cpp
int32_t Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution() const
```

## Remarques


Si la valeur de cette propriété est non nulle, elle limite la résolution des images raster exportées. Autrement dit, les images à haute résolution sont rééchantillonnées à la limite et les images à basse résolution sont exportées telles quelles.

Si la valeur de cette propriété est zéro, toutes les images raster sont exportées sans rééchantillonnage.

## Exemples



Montre comment définir une limite pour la résolution des images.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Voir aussi

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout méthode"
linktitle: "get_PageLayout"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout méthode. Obtient ou définit la mise en page utilisée lors du rendu de plusieurs pages en une seule sortie en C++."
type: docs
weight: 9500
url: /fr/cpp/aspose.words.saving/imagesaveoptions/get_pagelayout/
---
## ImageSaveOptions::get_PageLayout method


Obtient ou définit la disposition utilisée lors du rendu de plusieurs pages en une seule sortie.

```cpp
System::SharedPtr<Aspose::Words::Saving::MultiPageLayout> Aspose::Words::Saving::ImageSaveOptions::get_PageLayout() const
```

## Remarques


Utilisez l'une des méthodes d'usine de [MultiPageLayout](../../multipagelayout/) pour configurer cette propriété.

Pour [Tiff](../../../aspose.words/saveformat/) la valeur par défaut est [TiffFrames](../../multipagelayout/tiffframes/). Pour les autres formats la valeur par défaut est [SinglePage](../../multipagelayout/singlepage/).

Cette propriété n'a d'effet que lors de l'enregistrement aux formats suivants : [Jpeg](../../../aspose.words/saveformat/), [Gif](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Tiff](../../../aspose.words/saveformat/), [WebP](../)

## Exemples



Montre comment enregistrer le document en image JPG avec les paramètres de mise en page multi‑pages.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Configurez une mise en grille avec :
// - 3 colonnes par ligne.
// - Espacement de 10 pts entre les pages (horizontal et vertical).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Mises en page alternatives :
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Personnalisez l’arrière‑plan et la bordure.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## Voir aussi

* Class [MultiPageLayout](../../multipagelayout/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

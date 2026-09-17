---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution method"
linktitle: "get_ImageResolution"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution method. Spécifie la résolution de sortie pour les images lors de l'exportation vers Markdown. La valeur par défaut est %96 dpi en C++."
type: docs
weight: 3750
url: /fr/cpp/aspose.words.saving/markdownsaveoptions/get_imageresolution/
---
## MarkdownSaveOptions::get_ImageResolution method


Spécifie la résolution de sortie pour les images lors de l'exportation vers Markdown. La valeur par défaut est **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution() const
```


## Exemples



Montre comment définir la résolution de sortie pour les images.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ImageResolution(300);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

## Voir aussi

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

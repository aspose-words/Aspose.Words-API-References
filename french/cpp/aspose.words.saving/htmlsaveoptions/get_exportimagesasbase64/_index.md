---
title: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64"
linktitle: "get_ExportImagesAsBase64"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64. Spécifie si les images sont enregistrées au format Base64 dans le HTML, le MHTML ou l'EPUB de sortie. La valeur par défaut est false en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportimagesasbase64/
---
## HtmlSaveOptions::get_ExportImagesAsBase64 method


Spécifie si les images sont enregistrées au format Base64 dans le HTML, MHTML ou EPUB de sortie. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64() const
```

## Remarques


Lorsque cette propriété est définie sur **true**, les données d'images sont exportées directement dans les éléments **img** et aucun fichier séparé n'est créé.

## Exemples



Montre comment enregistrer un document .html avec des images intégrées à l'intérieur.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportImagesAsBase64(exportImagesAsBase64);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"<img src=\"data:image/png;base64") : outDocContents.Contains(u"<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```


Montre comment incorporer des polices dans un document HTML enregistré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontsAsBase64(true);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::Embedded);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

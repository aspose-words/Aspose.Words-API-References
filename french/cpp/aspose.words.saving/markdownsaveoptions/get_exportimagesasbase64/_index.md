---
title: "Méthode Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64"
linktitle: "get_ExportImagesAsBase64"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64. Spécifie si les images sont enregistrées au format Base64 dans le fichier de sortie. La valeur par défaut est false en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/markdownsaveoptions/get_exportimagesasbase64/
---
## MarkdownSaveOptions::get_ExportImagesAsBase64 method


Spécifie si les images sont enregistrées au format Base64 dans le fichier de sortie. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64() const
```

## Remarques


Lorsque cette propriété est définie sur **true**, les données d'images sont exportées directement dans les éléments **img** et aucun fichier séparé n'est créé.

## Exemples



Montre comment enregistrer un document .md avec des images intégrées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportImagesAsBase64(exportImagesAsBase64);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"data:image/jpeg;base64") : outDocContents.Contains(u"MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

## Voir aussi

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)

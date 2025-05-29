---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété MarkdownSaveOptions ExportImagesAsBase64 améliore vos fichiers de sortie en permettant l'enregistrement des images au format Base64. Valeur par défaut : false.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

Spécifie si les images sont enregistrées au format Base64 dans le fichier de sortie. La valeur par défaut est`FAUX` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Remarques

Lorsque cette propriété est définie sur`vrai` les données d'images sont exportées directement dans le**image** les éléments et les fichiers séparés ne sont pas créés.

## Exemples

Montre comment enregistrer un document .md avec des images intégrées à l'intérieur.

```csharp
Document doc = new Document(MyDir + "Images.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { ExportImagesAsBase64 = exportImagesAsBase64 };

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("data:image/jpeg;base64")
    : outDocContents.Contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

### Voir également

* class [MarkdownSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

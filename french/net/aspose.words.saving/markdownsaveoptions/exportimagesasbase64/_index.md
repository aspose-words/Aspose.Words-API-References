---
title: MarkdownSaveOptions.ExportImagesAsBase64
second_title: Référence de l'API Aspose.Words pour .NET
description: MarkdownSaveOptions propriété. Spécifie si les images sont enregistrées au format Base64 dans le fichier de sortie. La valeur par défaut estFAUX .
type: docs
weight: 20
url: /fr/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

Spécifie si les images sont enregistrées au format Base64 dans le fichier de sortie. La valeur par défaut est`FAUX` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

### Remarques

Lorsque cette propriété est définie sur`vrai` les données des images sont exportées directement dans le **img** les éléments et les fichiers séparés ne sont pas créés.

### Exemples

Montre comment enregistrer un document .md contenant des images intégrées.

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
* espace de noms [Aspose.Words.Saving](../../markdownsaveoptions/)
* Assemblée [Aspose.Words](../../../)



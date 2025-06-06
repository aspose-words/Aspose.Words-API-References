---
title: HtmlSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words pour .NET
description: Découvrez la propriété HtmlSaveOptions ExportImagesAsBase64 pour enregistrer les images au format Base64 et optimiser leur sortie HTML, MHTML ou EPUB. Améliorez la qualité de vos documents !
type: docs
weight: 170
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

Spécifie si les images sont enregistrées au format Base64 dans la sortie HTML, MHTML ou EPUB. La valeur par défaut est`FAUX` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Remarques

Lorsque cette propriété est définie sur`vrai` les données d'images sont exportées directement dans le**image** les éléments et les fichiers séparés ne sont pas créés.

## Exemples

Montre comment intégrer des polices dans un document HTML enregistré.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontsAsBase64 = true,
    CssStyleSheetType = CssStyleSheetType.Embedded,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

Montre comment enregistrer un document .html avec des images intégrées à l'intérieur.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportImagesAsBase64 = exportImagesAsBase64,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("<img src=\"data:image/png;base64")
    : outDocContents.Contains("<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

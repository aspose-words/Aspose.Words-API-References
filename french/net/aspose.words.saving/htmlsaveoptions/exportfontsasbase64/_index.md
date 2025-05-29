---
title: HtmlSaveOptions.ExportFontsAsBase64
linktitle: ExportFontsAsBase64
articleTitle: ExportFontsAsBase64
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété HtmlSaveOptions ExportFontsAsBase64 améliore votre code HTML en intégrant les polices encodées en Base64 pour de meilleures performances. Valeur par défaut : false.
type: docs
weight: 150
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportfontsasbase64/
---
## HtmlSaveOptions.ExportFontsAsBase64 property

Spécifie si les ressources de polices doivent être intégrées au HTML dans l'encodage Base64. La valeur par défaut est`FAUX` .

```csharp
public bool ExportFontsAsBase64 { get; set; }
```

## Remarques

Par défaut, les polices sont écrites dans des fichiers séparés. Si cette option est activée,`vrai`, les polices seront intégrées dans le CSS du document en encodage Base64.

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

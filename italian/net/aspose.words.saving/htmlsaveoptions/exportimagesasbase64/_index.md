---
title: HtmlSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ExportImagesAsBase64 proprietà. Specifica se le immagini vengono salvate in formato Base64 nelloutput HTML MHTML o EPUB. Limpostazione predefinita èfalso  in C#.
type: docs
weight: 170
url: /it/net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

Specifica se le immagini vengono salvate in formato Base64 nell'output HTML, MHTML o EPUB. L'impostazione predefinita è`falso` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Osservazioni

Quando questa proprietà è impostata su`VERO` i dati delle immagini vengono esportati direttamente nel file**img** non vengono creati elementi e file separati.

## Esempi

Mostra come incorporare i caratteri all'interno di un documento HTML salvato.

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

Mostra come salvare un documento .html con immagini incorporate al suo interno.

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

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)

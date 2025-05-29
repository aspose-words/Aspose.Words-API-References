---
title: HtmlSaveOptions.ExportFontsAsBase64
linktitle: ExportFontsAsBase64
articleTitle: ExportFontsAsBase64
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ExportFontsAsBase64 di HtmlSaveOptions migliora il tuo codice HTML incorporando i font nella codifica Base64 per prestazioni migliori. Il valore predefinito è false.
type: docs
weight: 150
url: /it/net/aspose.words.saving/htmlsaveoptions/exportfontsasbase64/
---
## HtmlSaveOptions.ExportFontsAsBase64 property

Specifica se le risorse dei font devono essere incorporate in HTML nella codifica Base64. Il valore predefinito è`falso` .

```csharp
public bool ExportFontsAsBase64 { get; set; }
```

## Osservazioni

Per impostazione predefinita, i font vengono scritti in file separati. Se questa opzione è impostata su`VERO`, i font verranno incorporati nel CSS del documento con codifica Base64.

## Esempi

Mostra come incorporare i font all'interno di un documento HTML salvato.

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

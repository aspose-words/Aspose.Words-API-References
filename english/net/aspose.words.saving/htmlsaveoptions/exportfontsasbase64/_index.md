---
title: HtmlSaveOptions.ExportFontsAsBase64
linktitle: ExportFontsAsBase64
second_title: Aspose.Words for .NET API Reference
description: HtmlSaveOptions ExportFontsAsBase64 property. Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is false in C#.
type: docs
weight: 160
url: /net/aspose.words.saving/htmlsaveoptions/exportfontsasbase64/
---
## HtmlSaveOptions.ExportFontsAsBase64 property

Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is `false`.

```csharp
public bool ExportFontsAsBase64 { get; set; }
```

## Remarks

By default, fonts are written to separate files. If this option is set to `true`, fonts will be embedded into the document's CSS in Base64 encoding.

## Examples

Shows how to embed fonts inside a saved HTML document.

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

Shows how to save a .html document with images embedded inside it.

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

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../htmlsaveoptions/)
* assembly [Aspose.Words](../../../)

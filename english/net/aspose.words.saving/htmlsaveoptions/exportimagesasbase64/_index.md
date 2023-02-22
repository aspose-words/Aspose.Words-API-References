---
title: ExportImagesAsBase64
second_title: Aspose.Words for .NET API Reference
description: HtmlSaveOptions property. Specifies whether images are saved in Base64 format to the output HTML MHTML or EPUB. Default is false in C#.
type: docs
weight: 180
url: /net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is `false`.

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Remarks

When this property is set to `true` images data are exported directly into the **img** elements and separate files are not created.

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

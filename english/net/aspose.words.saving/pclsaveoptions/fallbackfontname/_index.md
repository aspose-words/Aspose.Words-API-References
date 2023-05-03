---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
second_title: Aspose.Words for .NET API Reference
description: PclSaveOptions FallbackFontName property. Name of the font that will be used if no expected font is found in printer and builtin fonts collections in C#.
type: docs
weight: 20
url: /net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

Name of the font that will be used if no expected font is found in printer and built-in fonts collections.

```csharp
public string FallbackFontName { get; set; }
```

## Remarks

If no fallback is found, a warning is generated and "Arial" font is used.

## Examples

Shows how to declare a font that a printer will apply to printed text as a substitute should its original font be unavailable.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// This document will instruct the printer to apply "Times New Roman" to the text with the missing font.
// Should "Times New Roman" also be unavailable, the printer will default to the "Arial" font.
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### See Also

* class [PclSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pclsaveoptions/)
* assembly [Aspose.Words](../../../)

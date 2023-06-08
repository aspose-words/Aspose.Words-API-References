---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: Aspose.Words for .NET
description: PclSaveOptions AddPrinterFont method. Adds information about font that is uploaded to the printer by manufacturer in C#.
type: docs
weight: 50
url: /net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

Adds information about font that is uploaded to the printer by manufacturer.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fontFullName | String | Full name of the font (e.g. "Times New Roman Bold Italic"). |
| fontPclName | String | Name of the font that is used in Pcl document. |

## Remarks

There are 52 fonts that are to be built in any printer according to Pcl specification. However manufactures can add some other fonts to their devices.

## Examples

Shows how to get a printer to substitute all instances of a specific font with a different font.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// When printing this document, the printer will use the "Courier New" font
// to access places where our document used the "Courier" font.
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### See Also

* class [PclSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)

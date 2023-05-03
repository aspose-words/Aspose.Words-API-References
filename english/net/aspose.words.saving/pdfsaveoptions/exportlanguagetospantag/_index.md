---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
second_title: Aspose.Words for .NET API Reference
description: PdfSaveOptions ExportLanguageToSpanTag property. Gets or sets a value determining whether or not to create a Span tag in the document structure to export the text language in C#.
type: docs
weight: 150
url: /net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## ExportLanguageToSpanTag property

Gets or sets a value determining whether or not to create a "Span" tag in the document structure to export the text language.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## Remarks

Default value is `false` and "Lang" attribute is attached to a marked-content sequence in a page content stream.

When the value is `true` "Span" tag is created for the text with non-default language and "Lang" attribute is attached to this tag.

This value is ignored when [`ExportDocumentStructure`](../exportdocumentstructure/) is `false`.

## Examples

Shows how to create a "Span" tag in the document structure to export the text language.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Note, when "ExportDocumentStructure" is false, "ExportLanguageToSpanTag" is ignored.
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pdfsaveoptions/)
* assembly [Aspose.Words](../../../)

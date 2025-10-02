---
title: PdfSaveOptions.ExportFloatingShapesAsInlineTag
linktitle: ExportFloatingShapesAsInlineTag
articleTitle: ExportFloatingShapesAsInlineTag
second_title: Aspose.Words for .NET
description: Define how floating shapes appear in PDF by setting ExportFloatingShapesAsInlineTag for precise structure and layout control.
type: docs
weight: 150
url: /net/aspose.words.saving/pdfsaveoptions/exportfloatingshapesasinlinetag/
---
## PdfSaveOptions.ExportFloatingShapesAsInlineTag property

Gets or sets a value determining whether floating shapes are exported as inline tags in the document structure.

```csharp
public bool ExportFloatingShapesAsInlineTag { get; set; }
```

## Remarks

Default value is `false` and floating shapes will be exported as block-level tags, placed after the paragraph in which they are anchored.

When the value is `true` floating shapes will be exported as inline tags, placed within the paragraph where they are anchored.

This value is ignored when [`ExportDocumentStructure`](../exportdocumentstructure/) is `false`.

## Examples

Shows how to export floating shapes as inline tags.

```csharp
Document doc = new Document(MyDir + "Floating object.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.ExportFloatingShapesAsInlineTag = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportFloatingShapesAsInlineTag.pdf", saveOptions);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)

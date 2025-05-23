---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words for .NET
description: Enhance document performance with the SaveOptions MemoryOptimization property. Control memory usage before saving, boosting efficiency and speed.
type: docs
weight: 100
url: /net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is `false`.

```csharp
public bool MemoryOptimization { get; set; }
```

## Remarks

Setting this option to `true` can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

## Examples

Shows an option to optimize memory consumption when rendering large documents to PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Set the "MemoryOptimization" property to "true" to lower the memory footprint of large documents' saving operations
// at the cost of increasing the duration of the operation.
// Set the "MemoryOptimization" property to "false" to save the document as a PDF normally.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### See Also

* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)

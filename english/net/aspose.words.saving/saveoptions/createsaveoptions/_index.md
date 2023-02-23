---
title: SaveOptions.CreateSaveOptions
linktitle: CreateSaveOptions
second_title: Aspose.Words for .NET API Reference
description: SaveOptions method. Creates a save options object of a class suitable for the specified save format in C#.
type: docs
weight: 10
url: /net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(SaveFormat) {#createsaveoptions}

Creates a save options object of a class suitable for the specified save format.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | SaveFormat | The save format for which to create a save options object. |

### Return Value

An object of a class that derives from [`SaveOptions`](../).

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../saveoptions/)
* assembly [Aspose.Words](../../../)

---

## CreateSaveOptions(string) {#createsaveoptions_1}

Creates a save options object of a class suitable for the file extension specified in the given file name.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The extension of this file name determines the class of the save options object to create. |

### Return Value

An object of a class that derives from [`SaveOptions`](../).

## Examples

Shows how to set a default template for documents that do not have attached templates.

```csharp
Document doc = new Document();

// Enable automatic style updating, but do not attach a template document.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Since there is no template document, the document had nowhere to track style changes.
// Use a SaveOptions object to automatically set a template
// if a document that we are saving does not have one.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### See Also

* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../saveoptions/)
* assembly [Aspose.Words](../../../)

---
title: PdfSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: PdfSaveOptions Clone method. Creates a deep clone of this object in C#.
type: docs
weight: 350
url: /net/aspose.words.saving/pdfsaveoptions/clone/
---
## PdfSaveOptions.Clone method

Creates a deep clone of this object.

```csharp
public PdfSaveOptions Clone()
```

## Examples

Shows how to update all the fields in a document immediately before saving it to PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert text with PAGE and NUMPAGES fields. These fields do not display the correct value in real time.
// We will need to manually update them using updating methods such as "Field.Update()", and "Document.UpdateFields()"
// each time we need them to display accurate values.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "UpdateFields" property to "false" to not update all the fields in a document right before a save operation.
// This is the preferable option if we know that all our fields will be up to date before saving.
// Set the "UpdateFields" property to "true" to iterate through all the document
// fields and update them before we save it as a PDF. This will make sure that all the fields will display
// the most accurate values in the PDF.
options.UpdateFields = updateFields;

// We can clone PdfSaveOptions objects.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)

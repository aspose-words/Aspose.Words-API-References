---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: Aspose.Words for .NET
description: Control page breaks with TxtSaveOptionsBase's ForcePageBreaks property. Ensure seamless exports and maintain document formatting effortlessly.
type: docs
weight: 30
url: /net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Allows to specify whether the page breaks should be preserved during export.

The default value is `false`.

```csharp
public bool ForcePageBreaks { get; set; }
```

## Remarks

The property affects only page breaks that are inserted explicitly into a document. It is not related to page breaks that MS Word automatically inserts at the end of each page.

## Examples

Shows how to specify whether to preserve page breaks when exporting a document to plaintext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save"
// method to modify how we save the document to plaintext.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// The Aspose.Words "Document" objects have page breaks, just like Microsoft Word documents.
// Save formats such as ".txt" are one continuous body of text without page breaks.
// Set the "ForcePageBreaks" property to "true" to preserve all page breaks in the form of '\f' characters.
// Set the "ForcePageBreaks" property to "false" to discard all page breaks.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// If we load a plaintext document with page breaks,
// the "Document" object will use them to split the body into pages.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.That(doc.PageCount, Is.EqualTo(forcePageBreaks ? 3 : 1));
```

### See Also

* class [TxtSaveOptionsBase](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)

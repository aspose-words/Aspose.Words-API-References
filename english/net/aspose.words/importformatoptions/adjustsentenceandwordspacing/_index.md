---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
linktitle: AdjustSentenceAndWordSpacing
second_title: Aspose.Words for .NET API Reference
description: ImportFormatOptions AdjustSentenceAndWordSpacing property. Gets or sets a boolean value that specifies whether to adjust sentence and word spacing automatically. The default value is false in C#.
type: docs
weight: 20
url: /net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

Gets or sets a boolean value that specifies whether to adjust sentence and word spacing automatically. The default value is `false`.

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

## Examples

Shows how to adjust sentence and word spacing automatically.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(srcDoc);
builder.Write("Dolor sit amet.");

builder = new DocumentBuilder(dstDoc);
builder.Write("Lorem ipsum.");

ImportFormatOptions options = new ImportFormatOptions() { AdjustSentenceAndWordSpacing = true };
builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

Assert.AreEqual("Lorem ipsum. Dolor sit amet.", dstDoc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### See Also

* class [ImportFormatOptions](../)
* namespace [Aspose.Words](../../importformatoptions/)
* assembly [Aspose.Words](../../../)

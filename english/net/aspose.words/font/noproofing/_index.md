---
title: Font.NoProofing
linktitle: NoProofing
second_title: Aspose.Words for .NET API Reference
description: Font property. True when the formatted characters are not to be spell checked in C#.
type: docs
weight: 280
url: /net/aspose.words/font/noproofing/
---
## Font.NoProofing property

True when the formatted characters are not to be spell checked.

```csharp
public bool NoProofing { get; set; }
```

## Examples

Shows how to prevent text from being spell checked by Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normally, Microsoft Word emphasizes spelling errors with a jagged red underline.
// We can un-set the "NoProofing" flag to create a portion of text that
// bypasses the spell checker while completely disabling it.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)

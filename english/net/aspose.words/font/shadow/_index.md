---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words for .NET
description: Font Shadow property. True if the font is formatted as shadowed in C#.
type: docs
weight: 330
url: /net/aspose.words/font/shadow/
---
## Font.Shadow property

True if the font is formatted as shadowed.

```csharp
public bool Shadow { get; set; }
```

## Examples

Shows how to create a run of text formatted with a shadow.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Set the Shadow flag to apply an offset shadow effect,
// making it look like the letters are floating above the page.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

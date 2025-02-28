---
title: HyphenationOptions.ConsecutiveHyphenLimit
linktitle: ConsecutiveHyphenLimit
articleTitle: ConsecutiveHyphenLimit
second_title: Aspose.Words for .NET
description: Discover the ConsecutiveHyphenLimit property in HyphenationOptions. Control hyphen usage in your text for improved readability and formatting. Default: 0.
type: docs
weight: 30
url: /net/aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/
---
## HyphenationOptions.ConsecutiveHyphenLimit property

Gets or sets the maximum number of consecutive lines that can end with hyphens. Default value for this property is 0.

```csharp
public int ConsecutiveHyphenLimit { get; set; }
```

## Remarks

If value of this property is set to 0, any number of consecutive lines can end with hyphens.

The property does not have effect when saving to fixed page formats e.g. PDF.

## Examples

Shows how to configure automatic hyphenation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### See Also

* class [HyphenationOptions](../)
* namespace [Aspose.Words.Settings](../../../aspose.words.settings/)
* assembly [Aspose.Words](../../../)

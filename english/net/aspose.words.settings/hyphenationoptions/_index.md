---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Settings.HyphenationOptions class to effortlessly customize hyphenation settings for your documents and enhance text presentation.
type: docs
weight: 6630
url: /net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Allows to configure document hyphenation options.

To learn more, visit the [Working with Hyphenation](https://docs.aspose.com/words/net/working-with-hyphenation/) documentation article.

```csharp
public class HyphenationOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [HyphenationOptions](hyphenationoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Gets or sets value determining whether automatic hyphenation is turned on for the document. Default value for this property is `false`. |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Gets or sets the maximum number of consecutive lines that can end with hyphens. Default value for this property is 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Gets or sets value determining whether words written in all capital letters are hyphenated. Default value for this property is `true`. |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Gets or sets the distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. Default value for this property is 360 (0.25 inch). |

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

* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)

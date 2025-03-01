---
title: HyphenationOptions.AutoHyphenation
linktitle: AutoHyphenation
articleTitle: AutoHyphenation
second_title: Aspose.Words for .NET
description: Control automatic hyphenation with the HyphenationOptions property. Easily enhance your document's readability by toggling this feature on or off.
type: docs
weight: 20
url: /net/aspose.words.settings/hyphenationoptions/autohyphenation/
---
## HyphenationOptions.AutoHyphenation property

Gets or sets value determining whether automatic hyphenation is turned on for the document. Default value for this property is `false`.

```csharp
public bool AutoHyphenation { get; set; }
```

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

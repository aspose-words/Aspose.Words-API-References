---
title: Document.HyphenationOptions
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words for .NET
description: Explore the Document HyphenationOptions property to customize hyphenation settings, enhancing readability and improving your document's presentation.
type: docs
weight: 220
url: /net/aspose.words/document/hyphenationoptions/
---
## Document.HyphenationOptions property

Provides access to document hyphenation options.

```csharp
public HyphenationOptions HyphenationOptions { get; }
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

* class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

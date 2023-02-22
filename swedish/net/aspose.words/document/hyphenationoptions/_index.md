---
title: Document.HyphenationOptions
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Ger tillgång till alternativ för dokumentavstavning.
type: docs
weight: 210
url: /sv/net/aspose.words/document/hyphenationoptions/
---
## Document.HyphenationOptions property

Ger tillgång till alternativ för dokumentavstavning.

```csharp
public HyphenationOptions HyphenationOptions { get; }
```

### Exempel

Visar hur du konfigurerar automatisk avstavning.

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

### Se även

* class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)



---
title: SplitOptions.SplitCriteria
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen SplitOptions SplitCriteria förbättrar dokumenthanteringen genom att effektivt dela upp ditt innehåll i hanterbara avsnitt.
type: docs
weight: 20
url: /sv/net/aspose.words.lowcode/splitoptions/splitcriteria/
---
## SplitOptions.SplitCriteria property

Anger kriterierna för att dela upp dokumentet i delar.

```csharp
public SplitCriteria SplitCriteria { get; set; }
```

## Exempel

Visar hur man delar upp dokumentet efter sidor.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Se även

* enum [SplitCriteria](../../splitcriteria/)
* class [SplitOptions](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

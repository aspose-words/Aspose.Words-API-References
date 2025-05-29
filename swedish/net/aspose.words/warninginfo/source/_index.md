---
title: WarningInfo.Source
linktitle: Source
articleTitle: Source
second_title: Aspose.Words för .NET
description: Upptäck egenskapen WarningInfo Source som avslöjar ursprunget till varningar, vilket förbättrar programmets tillförlitlighet och användarupplevelse.
type: docs
weight: 20
url: /sv/net/aspose.words/warninginfo/source/
---
## WarningInfo.Source property

Returnerar källan till varningen.

```csharp
public WarningSource Source { get; }
```

## Exempel

Visar hur man arbetar med varningskällan.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Se även

* enum [WarningSource](../../warningsource/)
* class [WarningInfo](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

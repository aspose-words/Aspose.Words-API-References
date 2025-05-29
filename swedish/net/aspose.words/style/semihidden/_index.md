---
title: Style.SemiHidden
linktitle: SemiHidden
articleTitle: SemiHidden
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen SemiHidden styr stilens synlighet i stilgalleriet och åtgärdsfönstret, vilket förbättrar ditt designarbetsflöde och effektivitet.
type: docs
weight: 170
url: /sv/net/aspose.words/style/semihidden/
---
## Style.SemiHidden property

Hämtar/ställer in om stilen ska döljas från stilgalleriet och från åtgärdsfönstret Stilar.

```csharp
public bool SemiHidden { get; set; }
```

## Exempel

Visar hur man prioriterar och döljer en stil.

```csharp
Document doc = new Document();
Style styleTitle = doc.Styles[StyleIdentifier.Subtitle];

if (styleTitle.Priority == 9)
    styleTitle.Priority = 10;

if (!styleTitle.UnhideWhenUsed)
    styleTitle.UnhideWhenUsed = true;

if (styleTitle.SemiHidden)
    styleTitle.SemiHidden = true;

doc.Save(ArtifactsDir + "Styles.StylePriority.docx");
```

### Se även

* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

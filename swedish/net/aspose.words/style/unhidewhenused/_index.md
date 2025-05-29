---
title: Style.UnhideWhenUsed
linktitle: UnhideWhenUsed
articleTitle: UnhideWhenUsed
second_title: Aspose.Words för .NET
description: Upptäck hur du hanterar egenskapen UnhideWhenUsed för format. Kontrollera synligheten i formatgalleriet och åtgärdsfönstret för att förbättra dokumentets design.
type: docs
weight: 210
url: /sv/net/aspose.words/style/unhidewhenused/
---
## Style.UnhideWhenUsed property

Hämtar/ställer in om stilen som används i det aktuella dokumentet ska visas i stilgalleriet och i åtgärdsfönstret Stilar. Sant när den använda stilen ska visas i stilgalleriet.

```csharp
public bool UnhideWhenUsed { get; set; }
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

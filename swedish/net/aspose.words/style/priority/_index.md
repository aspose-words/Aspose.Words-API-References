---
title: Style.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words för .NET
description: Upptäck hur du hanterar inställningar för stilprioritet för att optimera stilsortering i aktivitetsfönstret. Förbättra ditt arbetsflöde med effektiv stilorganisation!
type: docs
weight: 160
url: /sv/net/aspose.words/style/priority/
---
## Style.Priority property

Hämtar/ställer in heltalsvärdet som representerar prioriteten för sortering av formaten i åtgärdsfönstret Format.

```csharp
public int Priority { get; set; }
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

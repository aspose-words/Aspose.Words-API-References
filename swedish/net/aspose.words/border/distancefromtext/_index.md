---
title: Border.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Border DistanceFromText för att enkelt justera kantavståndet från text eller sidkanter i punkter för förbättrad layoutkontroll.
type: docs
weight: 20
url: /sv/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Hämtar eller ställer in avståndet mellan kantlinjen och texten eller sidkanten i punkter.

```csharp
public double DistanceFromText { get; set; }
```

## Anmärkningar

Har ingen effekt och återställs automatiskt till noll för kantlinjer runt tabellceller.

## Exempel

Visar hur man skapar en bred blå kantlinje högst upp på första sidan.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### Se även

* class [Border](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

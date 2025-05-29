---
title: PageSetup.BorderAlwaysInFront
linktitle: BorderAlwaysInFront
articleTitle: BorderAlwaysInFront
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup BorderAlwaysInFront för att optimera sidkanter, förbättra layout och synlighet för korsande texter och objekt.
type: docs
weight: 20
url: /sv/net/aspose.words/pagesetup/borderalwaysinfront/
---
## PageSetup.BorderAlwaysInFront property

Anger var sidkantlinjen är placerad i förhållande till korsande texter och objekt.

```csharp
public bool BorderAlwaysInFront { get; set; }
```

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

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

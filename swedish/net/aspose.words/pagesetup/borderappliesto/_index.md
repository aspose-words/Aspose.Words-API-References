---
title: PageSetup.BorderAppliesTo
linktitle: BorderAppliesTo
articleTitle: BorderAppliesTo
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen PageSetup BorderAppliesTo förbättrar din dokumentlayout genom att styra utskrift av sidkanter för ett elegant och professionellt utseende.
type: docs
weight: 30
url: /sv/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

Anger vilka sidor sidkantlinjen skrivs ut på.

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
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

* enum [PageBorderAppliesTo](../../pageborderappliesto/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

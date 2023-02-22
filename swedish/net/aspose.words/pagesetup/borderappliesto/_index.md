---
title: PageSetup.BorderAppliesTo
second_title: Aspose.Words för .NET API Referens
description: PageSetup fast egendom. Anger vilka sidor som sidkanten skrivs ut på.
type: docs
weight: 30
url: /sv/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

Anger vilka sidor som sidkanten skrivs ut på.

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
```

### Exempel

Visar hur man skapar en bred blå bandkant längst upp på första sidan.

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
* namnutrymme [Aspose.Words](../../pagesetup/)
* hopsättning [Aspose.Words](../../../)



---
title: BorderAlwaysInFront
second_title: Aspose.Words för .NET API Referens
description: Anger var sidkanten är placerad i förhållande till korsande texter och objekt.
type: docs
weight: 20
url: /sv/net/aspose.words/pagesetup/borderalwaysinfront/
---
## PageSetup.BorderAlwaysInFront property

Anger var sidkanten är placerad i förhållande till korsande texter och objekt.

```csharp
public bool BorderAlwaysInFront { get; set; }
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

* class [PageSetup](../../pagesetup)
* namnutrymme [Aspose.Words](../../pagesetup)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

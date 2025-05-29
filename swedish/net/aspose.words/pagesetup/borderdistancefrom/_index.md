---
title: PageSetup.BorderDistanceFrom
linktitle: BorderDistanceFrom
articleTitle: BorderDistanceFrom
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup BorderDistanceFrom för att kontrollera sidkantmätningar för exakt dokumentformatering. Förbättra din layout idag!
type: docs
weight: 40
url: /sv/net/aspose.words/pagesetup/borderdistancefrom/
---
## PageSetup.BorderDistanceFrom property

Hämtar eller anger ett värde som anger om den angivna sidkanten mäts från sidans kant eller från texten den omger.

```csharp
public PageBorderDistanceFrom BorderDistanceFrom { get; set; }
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

* enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

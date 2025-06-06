---
title: PageBorderDistanceFrom Enum
linktitle: PageBorderDistanceFrom
articleTitle: PageBorderDistanceFrom
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.PageBorderDistanceFrom-enumereringen för exakt placering av sidkanter. Förbättra dokumentformateringen med optimal marginalplacering.
type: docs
weight: 5080
url: /sv/net/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enumeration

Anger sidkantens placering i förhållande till sidmarginalen.

```csharp
public enum PageBorderDistanceFrom
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Text | `0` | Kantpositionen mäts från sidmarginalen. |
| PageEdge | `1` | Kantpositionen mäts från sidans kant. |

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

* class [PageSetup](../pagesetup/)
* property [BorderDistanceFrom](../pagesetup/borderdistancefrom/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)

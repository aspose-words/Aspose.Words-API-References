---
title: Enum PageBorderAppliesTo
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.PageBorderAppliesTo uppräkning. Anger vilka sidor som sidkanten skrivs ut på.
type: docs
weight: 4100
url: /sv/net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

Anger vilka sidor som sidkanten skrivs ut på.

```csharp
public enum PageBorderAppliesTo
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| AllPages | `0` | Sidkanten visas på alla sidor i avsnittet. |
| FirstPage | `1` | Sidkanten visas endast på första sidan i avsnittet. |
| OtherPages | `2` | Sidkanten visas på alla sidor utom den första sidan i avsnittet. |

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

* class [PageSetup](../pagesetup/)
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)



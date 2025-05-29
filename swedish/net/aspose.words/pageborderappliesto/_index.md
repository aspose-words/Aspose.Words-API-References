---
title: PageBorderAppliesTo Enum
linktitle: PageBorderAppliesTo
articleTitle: PageBorderAppliesTo
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.PageBorderAppliesTo för att styra utskrift av sidkanter över specifika sidor för förbättrad dokumentformatering.
type: docs
weight: 5070
url: /sv/net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

Anger vilka sidor sidkantlinjen skrivs ut på.

```csharp
public enum PageBorderAppliesTo
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| AllPages | `0` | Sidkantlinjen visas på alla sidor i avsnittet. |
| FirstPage | `1` | Sidkantlinjen visas endast på avsnittets första sida. |
| OtherPages | `2` | Sidkantlinjen visas på alla sidor utom den första sidan i avsnittet. |

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
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)

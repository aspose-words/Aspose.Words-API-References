---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: Aspose.Words för .NET
description: Upptäck TabStopCollection GetPositionByIndex-metoden för att enkelt hitta tabbstoppspositioner i punkter efter index. Optimera din layout utan ansträngning!
type: docs
weight: 100
url: /sv/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Hämtar positionen (i punkter) för tabbstoppet vid det angivna indexet.

```csharp
public double GetPositionByIndex(int index)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | Int32 | Ett index till samlingen av tabulaturer. |

### Returvärde

Tabstoppets position.

## Exempel

Visar hur man hittar en flik, stannar till vid dess index och verifierar dess position.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// Verifiera positionen för det andra tabbstoppet i samlingen.
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### Se även

* class [TabStopCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

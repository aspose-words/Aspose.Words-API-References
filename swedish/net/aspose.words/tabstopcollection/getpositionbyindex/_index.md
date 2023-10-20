---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: Aspose.Words för .NET
description: TabStopCollection GetPositionByIndex metod. Hämtar positionen i poäng för tabbstoppet vid det angivna indexet i C#.
type: docs
weight: 100
url: /sv/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Hämtar positionen (i poäng) för tabbstoppet vid det angivna indexet.

```csharp
public double GetPositionByIndex(int index)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | Int32 | Ett index över samlingen av tabbstopp. |

### Returvärde

Tabstoppets läge.

## Exempel

Visar hur du hittar en flik, stannar vid dess index och verifierar dess position.

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

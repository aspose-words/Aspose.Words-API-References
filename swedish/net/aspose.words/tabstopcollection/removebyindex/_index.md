---
title: TabStopCollection.RemoveByIndex
second_title: Aspose.Words för .NET API Referens
description: TabStopCollection metod. Tar bort ett tabbstopp vid det angivna indexet från samlingen.
type: docs
weight: 110
url: /sv/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

Tar bort ett tabbstopp vid det angivna indexet från samlingen.

```csharp
public void RemoveByIndex(int index)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | Int32 | Ett index över samlingen av tabbstopp. |

### Exempel

Visar hur man väljer ett tabbstopp i ett dokument efter dess index och tar bort det.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// Ta bort det första tabbstoppet.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### Se även

* class [TabStopCollection](../)
* namnutrymme [Aspose.Words](../../tabstopcollection/)
* hopsättning [Aspose.Words](../../../)



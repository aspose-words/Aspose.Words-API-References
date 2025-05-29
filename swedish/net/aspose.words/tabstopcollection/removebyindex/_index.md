---
title: TabStopCollection.RemoveByIndex
linktitle: RemoveByIndex
articleTitle: RemoveByIndex
second_title: Aspose.Words för .NET
description: Hantera enkelt dina tabbstopp med metoden RemoveByIndex. Ta snabbt bort alla tabbstopp från din samling för en strömlinjeformad design.
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
| index | Int32 | Ett index till samlingen av tabulaturer. |

## Exempel

Visar hur man markerar och tar bort ett tabbstopp i ett dokument med hjälp av dess index.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// Ta bort den första tabbstoppen.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### Se även

* class [TabStopCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

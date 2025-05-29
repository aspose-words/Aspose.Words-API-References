---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: Aspose.Words für .NET
description: Entdecken Sie die TabStopCollection GetIndexByPosition-Methode, um den Index eines Tabstopps an einer beliebigen Punktposition einfach zu finden. Perfekt für präzise Layoutkontrolle!
type: docs
weight: 90
url: /de/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Ruft den Index eines Tabulators mit der angegebenen Position in Punkten ab.

```csharp
public int GetIndexByPosition(double position)
```

## Beispiele

Zeigt, wie Sie eine Position nachschlagen, um festzustellen, ob dort ein Tabulator vorhanden ist, und wie Sie dessen Index abrufen.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Fügen Sie an einer Position von 30 mm einen Tabulator hinzu.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// Ein von "GetIndexByPosition" zurückgegebenes Ergebnis von "0" bestätigt, dass ein Tabstopp
// bei 30 mm ist in dieser Sammlung vorhanden und befindet sich am Index 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// Eine von "GetIndexByPosition" zurückgegebene "-1" bestätigt, dass
// In dieser Sammlung gibt es keinen Tabstopp mit einer Position von 60 mm.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Siehe auch

* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

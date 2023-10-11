---
title: TabStopCollection.GetIndexByPosition
second_title: Aspose.Words für .NET-API-Referenz
description: TabStopCollection methode. Ruft den Index eines Tabstopps mit der angegebenen Position in Punkten ab.
type: docs
weight: 90
url: /de/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Ruft den Index eines Tabstopps mit der angegebenen Position in Punkten ab.

```csharp
public int GetIndexByPosition(double position)
```

### Beispiele

Zeigt, wie man eine Position nachschlägt, um zu sehen, ob dort ein Tabstopp vorhanden ist, und um seinen Index zu erhalten.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Fügen Sie einen Tabstopp an einer Position von 30 mm hinzu.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// Ein von „GetIndexByPosition“ zurückgegebenes Ergebnis „0“ bestätigt, dass ein Tabstopp vorliegt
// bei 30 mm ist in dieser Sammlung vorhanden und hat den Index 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// Ein von „GetIndexByPosition“ zurückgegebenes „-1“ bestätigt dies
// In dieser Sammlung gibt es keinen Tabstopp mit einer Position von 60 mm.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Siehe auch

* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../tabstopcollection/)
* Montage [Aspose.Words](../../../)



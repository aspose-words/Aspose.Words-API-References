---
title: TabStopCollection.GetPositionByIndex
second_title: Aspose.Words für .NET-API-Referenz
description: TabStopCollection methode. Ruft die Position in Punkten des Tabstopps am angegebenen Index ab.
type: docs
weight: 100
url: /de/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Ruft die Position (in Punkten) des Tabstopps am angegebenen Index ab.

```csharp
public double GetPositionByIndex(int index)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Ein Index in die Sammlung von Tabstopps. |

### Rückgabewert

Die Position des Tabstopps.

### Beispiele

Zeigt, wie Sie einen Tab finden, bei seinem Index anhalten und seine Position überprüfen.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// Überprüfen Sie die Position des zweiten Tabstopps in der Auflistung.
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### Siehe auch

* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../tabstopcollection/)
* Montage [Aspose.Words](../../../)



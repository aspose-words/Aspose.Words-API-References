---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: Aspose.Words für .NET
description: Entdecken Sie die TabStopCollection GetPositionByIndex-Methode, um Tabstopppositionen einfach in Punkten nach Index zu finden. Optimieren Sie Ihr Layout mühelos!
type: docs
weight: 100
url: /de/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Ruft die Position (in Punkten) des Tabulatorstopps am angegebenen Index ab.

```csharp
public double GetPositionByIndex(int index)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Ein Index in der Sammlung von Tabstopps. |

### Rückgabewert

Die Position des Tabstopps.

## Beispiele

Zeigt, wie Sie eine Registerkarte finden, an ihrem Index anhalten und ihre Position überprüfen.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// Überprüfen Sie die Position des zweiten Tabulatorstopps in der Sammlung.
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### Siehe auch

* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

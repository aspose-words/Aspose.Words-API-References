---
title: TabStopCollection.RemoveByIndex
linktitle: RemoveByIndex
articleTitle: RemoveByIndex
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihre Tabstopps mühelos mit der RemoveByIndex-Methode. Entfernen Sie schnell beliebige Tabstopps aus Ihrer Sammlung für ein optimiertes Design.
type: docs
weight: 110
url: /de/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

Entfernt einen Tabulatorstopp am angegebenen Index aus der Auflistung.

```csharp
public void RemoveByIndex(int index)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Ein Index in der Sammlung von Tabstopps. |

## Beispiele

Zeigt, wie Sie einen Tabulator in einem Dokument anhand seines Index auswählen und entfernen.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// Den ersten Tabulator entfernen.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### Siehe auch

* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

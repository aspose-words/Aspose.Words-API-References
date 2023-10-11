---
title: TabStopCollection.RemoveByIndex
second_title: Aspose.Words für .NET-API-Referenz
description: TabStopCollection methode. Entfernt einen Tabstopp am angegebenen Index aus der Sammlung.
type: docs
weight: 110
url: /de/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

Entfernt einen Tabstopp am angegebenen Index aus der Sammlung.

```csharp
public void RemoveByIndex(int index)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Ein Index in der Sammlung von Tabstopps. |

### Beispiele

Zeigt, wie man einen Tabstopp in einem Dokument anhand seines Index auswählt und entfernt.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// Den ersten Tabstopp entfernen.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### Siehe auch

* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../tabstopcollection/)
* Montage [Aspose.Words](../../../)



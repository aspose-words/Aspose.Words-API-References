---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: Aspose.Words för .NET
description: Upptäck TabStopCollection GetIndexByPosition-metoden för att enkelt hitta indexet för ett tabbstopp vid vilken punktposition som helst. Perfekt för exakt layoutkontroll!
type: docs
weight: 90
url: /sv/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Hämtar indexet för ett tabbstopp med den angivna positionen i punkter.

```csharp
public int GetIndexByPosition(double position)
```

## Exempel

Visar hur man slår upp en position för att se om det finns ett tabbstopp där och hämtar dess index.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Lägg till ett tabbstopp vid en position av 30 mm.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// Ett resultat av "0" som returneras av "GetIndexByPosition" bekräftar att ett tabbstopp
// vid 30mm finns i den här samlingen, och den är vid index 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// Ett "-1" som returneras av "GetIndexByPosition" bekräftar att
// det finns inget tabbstopp i den här samlingen med positionen 60 mm.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Se även

* class [TabStopCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

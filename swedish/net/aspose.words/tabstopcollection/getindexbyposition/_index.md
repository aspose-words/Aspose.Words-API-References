---
title: TabStopCollection.GetIndexByPosition
second_title: Aspose.Words för .NET API Referens
description: TabStopCollection metod. Hämtar indexet för ett tabbstopp med angiven position i poäng.
type: docs
weight: 90
url: /sv/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Hämtar indexet för ett tabbstopp med angiven position i poäng.

```csharp
public int GetIndexByPosition(double position)
```

### Exempel

Visar hur man slår upp en position för att se om ett tabbstopp finns där och erhåller dess index.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Lägg till ett tabbstopp i en position på 30 mm.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// Ett resultat av "0" returnerat av "GetIndexByPosition" bekräftar att ett tabbstopp
// på 30 mm finns i denna samling, och den är på index 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// En "-1" som returneras av "GetIndexByPosition" bekräftar det
// det finns inget tabbstopp i denna samling med en position på 60 mm.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Se även

* class [TabStopCollection](../)
* namnutrymme [Aspose.Words](../../tabstopcollection/)
* hopsättning [Aspose.Words](../../../)



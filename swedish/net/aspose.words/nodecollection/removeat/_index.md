---
title: NodeCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words för .NET
description: NodeCollection RemoveAt metod. Tar bort noden vid det angivna indexet från samlingen och från dokumentet i C#.
type: docs
weight: 100
url: /sv/net/aspose.words/nodecollection/removeat/
---
## NodeCollection.RemoveAt method

Tar bort noden vid det angivna indexet från samlingen och från dokumentet.

```csharp
public void RemoveAt(int index)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | Int32 | Det nollbaserade indexet för noden. Negativa index är tillåtna och indikerar åtkomst från baksidan av listan. Till exempel betyder -1 den sista noden, -2 betyder näst före sist och så vidare. |

## Exempel

Visar hur man lägger till och tar bort avsnitt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Ta bort det första avsnittet från dokumentet.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Lägg till en kopia av det som nu är det första avsnittet i slutet av dokumentet.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Se även

* class [NodeCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

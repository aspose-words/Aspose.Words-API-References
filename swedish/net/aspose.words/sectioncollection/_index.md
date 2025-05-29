---
title: SectionCollection Class
linktitle: SectionCollection
articleTitle: SectionCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.SectionCollection – din lösning för att hantera dokumentavsnitt effektivt med kraftfulla funktioner och flexibilitet.
type: docs
weight: 6570
url: /sv/net/aspose.words/sectioncollection/
---
## SectionCollection class

En samling av[`Section`](../section/) objekt i dokumentet.

För att lära dig mer, besök[Arbeta med sektioner](https://docs.aspose.com/words/net/working-with-sections/) dokumentationsartikel.

```csharp
public class SectionCollection : NodeCollection
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Hämtar antalet noder i samlingen. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | Hämtar ett avsnitt vid det angivna indexet. (2 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Lägger till en nod i slutet av samlingen. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tar bort alla noder från den här samlingen och från dokumentet. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Avgör om en nod finns i samlingen. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Ger en enkel iteration i "foreach"-stil över samlingen av noder. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Infogar en nod i samlingen vid det angivna indexet. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Tar bort noden vid det angivna indexet från samlingen och från dokumentet. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | Kopierar alla avsnitt från samlingen till en ny array med avsnitt. (2 methods) |

## Anmärkningar

Ett Microsoft Word-dokument kan innehålla flera avsnitt. För att skapa ett avsnitt i ett Microsoft Word-dokument, välj kommandot Infoga/Bryt och välj en brytningstyp. Bryten anger om avsnittet börjar på en ny sida eller på samma sida.

Programmatiskt infoga och ta bort avsnitt kan användas för att anpassa dokument som produceras under koppling av dokument. Om ett dokument behöver ha olika innehåll eller delar av innehållet beroende på vissa kriterier kan du skapa ett "huvuddokument" som innehåller flera avsnitt och ta bort några av avsnitten före eller efter koppling av dokument.

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

* class [NodeCollection](../nodecollection/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)

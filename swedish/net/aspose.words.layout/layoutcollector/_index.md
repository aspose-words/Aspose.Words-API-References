---
title: Class LayoutCollector
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Layout.LayoutCollector klass. Denna klass gör det möjligt att beräkna sidnummer för dokumentnoder.
type: docs
weight: 3320
url: /sv/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Denna klass gör det möjligt att beräkna sidnummer för dokumentnoder.

För att lära dig mer, besök[Konvertera till fastsidesformat](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) dokumentationsartikel.

```csharp
public class LayoutCollector
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [LayoutCollector](layoutcollector/)(Document) | Initierar en instans av denna klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Hämtar eller ställer in dokumentet som denna samlarinstans är bifogad till. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Rensar alla insamlade layoutdata. Anrop den här metoden efter att dokumentet har uppdaterats manuellt eller efter att layouten byggts om. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(Node) | Hämtar 1-baserat index på sidan där noden slutar. Returnerar 0 om noden inte kan mappas till en sida. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(Node) | Returnerar en ogenomskinlig position för[`LayoutEnumerator`](../layoutenumerator/) som motsvarar den angivna noden. Du kan använda returnerat värde som ett argument till[`Current`](../layoutenumerator/current/) givet att dokumentet som räknas upp och dokumentet för noden är desamma. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(Node) | Hämtar antal sidor som den angivna noden sträcker sig över. 0 om noden är inom en enda sida. Detta är samma sak som[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(Node) | Hämtar 1-baserat index på sidan där noden börjar. Returnerar 0 om noden inte kan mappas till en sida. |

### Anmärkningar

När du skapar en`LayoutCollector` och ange a[`Document`](../../aspose.words/document/) dokumentobjekt att bifoga till, samlaren kommer att spela in mappning av dokumentnoder till layoutobjekt när dokumentet formateras till sidor.

Du kommer att kunna ta reda på vilken sida en viss dokumentnod (t.ex. körning, stycke eller tabellcell) finns genom att använda[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) och[`GetNumPagesSpanned`](./getnumpagesspanned/)metoder. Dessa metoder bygger automatiskt en sidlayoutmodell av dokumentet och uppdaterar fält om det behövs.

När du inte längre behöver samla in layoutinformation är det bäst att ställa in[`Document`](./document/) egendom till`null` för att undvika onödig insamling av fler layoutmappningar.

### Exempel

Visar hur man kan se sidorna som en nod sträcker sig över.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Kalla metoden "GetNumPagesSpanned" för att räkna hur många sidor innehållet i vårt dokument sträcker sig.
// Eftersom dokumentet är tomt är antalet sidor för närvarande noll.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Fyll dokumentet med 5 sidor innehåll.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Innan layoutsamlaren måste vi anropa metoden "UpdatePageLayout" för att ge oss
// en korrekt siffra för alla layoutrelaterade mätvärden, till exempel sidantal.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Vi kan se numren på start- och slutsidorna för alla noder och deras övergripande sidspann.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Vi kan iterera över layoutentiteterna med hjälp av en LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumeratorn kan gå igenom samlingen av layoutentiteter som ett träd.
// Vi kan också tillämpa det på valfri nods motsvarande layoutentitet.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Se även

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)



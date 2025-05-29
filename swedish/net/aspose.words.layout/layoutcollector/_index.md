---
title: LayoutCollector Class
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Layout.LayoutCollector för att effektivt beräkna sidnummer i dokumentnoder och förbättra din dokumenthanteringsupplevelse.
type: docs
weight: 3770
url: /sv/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Den här klassen låter dig beräkna sidnummer för dokumentnoder.

För att lära dig mer, besök[Konvertera till fast sidformat](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) dokumentationsartikel.

```csharp
public class LayoutCollector
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [LayoutCollector](layoutcollector/)(*[Document](../../aspose.words/document/)*) | Initierar en instans av denna klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Hämtar eller ställer in dokumentet som denna insamlingsinstans är kopplad till. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Rensar all insamlad layoutdata. Anropar den här metoden efter att dokumentet har uppdaterats manuellt eller layouten har byggts om. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(*[Node](../../aspose.words/node/)*) | Hämtar ett 1-baserat index för sidan där noden slutar. Returnerar 0 om noden inte kan mappas till en sida. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(*[Node](../../aspose.words/node/)*) | Returnerar en ogenomskinlig position för[`LayoutEnumerator`](../layoutenumerator/) vilket motsvarar den angivna noden. Du kan använda returnerat värde som argument för att[`Current`](../layoutenumerator/current/) givet att dokumentet som räknas upp och nodens dokument är desamma. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(*[Node](../../aspose.words/node/)*) | Hämtar antalet sidor som den angivna noden sträcker sig över. 0 om noden finns inom en enda sida. Detta är samma sak som[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(*[Node](../../aspose.words/node/)*) | Hämtar ett 1-baserat index för sidan där noden börjar. Returnerar 0 om noden inte kan mappas till en sida. |

## Anmärkningar

När du skapar en`LayoutCollector` och ange en[`Document`](../../aspose.words/document/)dokumentobjekt att bifoga till, samlaren kommer att registrera mappning av dokumentnoder till layoutobjekt när dokumentet formateras till sidor.

Du kommer att kunna ta reda på på vilken sida en viss dokumentnod (t.ex. körning, stycke eller tabellcell) finns genom att använda[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) och[`GetNumPagesSpanned`](./getnumpagesspanned/) metoder. Dessa metoder bygger automatiskt en sidlayoutmodell för dokumentet och uppdaterar fält vid behov.

När du inte längre behöver samla in layoutinformation är det bäst att ställa in[`Document`](./document/) egendom till`null` för att undvika onödig insamling av fler layoutmappningar.

## Exempel

Visar hur man ser sidintervallen som en nod sträcker sig över.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Anropa metoden "GetNumPagesSpanned" för att räkna hur många sidor innehållet i vårt dokument sträcker sig över.
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

// Innan layoutinsamlaren anropar vi metoden "UpdatePageLayout" för att ge oss
// en korrekt siffra för alla layoutrelaterade mätvärden, såsom sidantal.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Vi kan se numren på start- och slutsidorna för valfri nod och deras totala sidlängd.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Vi kan iterera över layout-entiteterna med hjälp av en LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumeratorn kan gå igenom samlingen av layout-entiteter som ett träd.
// Vi kan också tillämpa den på vilken nods motsvarande layout-entitet som helst.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Se även

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)

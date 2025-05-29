---
title: LayoutCollector.GetEndPageIndex
linktitle: GetEndPageIndex
articleTitle: GetEndPageIndex
second_title: Aspose.Words för .NET
description: Upptäck LayoutCollectors GetEndPageIndex-metod för att enkelt hitta det 1-baserade indexet för en nods slutsida. Förenkla din sidmappning idag!
type: docs
weight: 40
url: /sv/net/aspose.words.layout/layoutcollector/getendpageindex/
---
## LayoutCollector.GetEndPageIndex method

Hämtar ett 1-baserat index för sidan där noden slutar. Returnerar 0 om noden inte kan mappas till en sida.

```csharp
public int GetEndPageIndex(Node node)
```

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

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)

---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: Aspose.Words för .NET
description: Upptäck LayoutCollector GetEntity-metoden, hämta enkelt LayoutEnumeratorns position för sömlös dokumentnavigering och förbättrad produktivitet.
type: docs
weight: 50
url: /sv/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Returnerar en ogenomskinlig position för[`LayoutEnumerator`](../../layoutenumerator/) vilket motsvarar den angivna noden. Du kan använda returnerat värde som argument för att[`Current`](../../layoutenumerator/current/) givet att dokumentet som räknas upp och nodens dokument är desamma.

```csharp
public object GetEntity(Node node)
```

## Anmärkningar

Den här metoden fungerar endast för[`Paragraph`](../../../aspose.words/paragraph/) noder, såväl som odelbara inline-noder, t.ex.[`BookmarkStart`](../../../aspose.words/bookmarkstart/) eller[`Shape`](../../../aspose.words.drawing/shape/) Det fungerar inte för[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) eller[`Table`](../../../aspose.words.tables/table/) noder och noder inom sidhuvud/sidfot.

Observera att entiteten returnerades för en[`Paragraph`](../../../aspose.words/paragraph/)noden är ett styckebrytningsintervall. Använd lämplig metod för att gå upp till den överordnade raden

Om du behöver navigera till en[`Run`](../../../aspose.words/run/) av text kan du infoga ett bokmärke precis före it och sedan navigera till bokmärket istället.

Om du behöver navigera till en[`Cell`](../../../aspose.words.tables/cell/) noden så kan du flytta till en[`Paragraph`](../../../aspose.words/paragraph/) nod i den här cellen och sedan stiga upp till en förälderenhet. Samma metod kan användas för[`Row`](../../../aspose.words.tables/row/) och[`Table`](../../../aspose.words.tables/table/) noder.

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

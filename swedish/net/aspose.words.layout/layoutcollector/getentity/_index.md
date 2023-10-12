---
title: LayoutCollector.GetEntity
second_title: Aspose.Words för .NET API Referens
description: LayoutCollector metod. Returnerar en ogenomskinlig position förLayoutEnumerator som motsvarar den angivna noden. Du kan använda returnerat värde som ett argument tillCurrent givet att dokumentet som räknas upp och dokumentet för noden är desamma.
type: docs
weight: 50
url: /sv/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Returnerar en ogenomskinlig position för[`LayoutEnumerator`](../../layoutenumerator/) som motsvarar den angivna noden. Du kan använda returnerat värde som ett argument till[`Current`](../../layoutenumerator/current/) givet att dokumentet som räknas upp och dokumentet för noden är desamma.

```csharp
public object GetEntity(Node node)
```

### Anmärkningar

Denna metod fungerar endast för[`Paragraph`](../../../aspose.words/paragraph/) noder, såväl som odelbara inline-noder, t.ex[`BookmarkStart`](../../../aspose.words/bookmarkstart/) eller[`Shape`](../../../aspose.words.drawing/shape/) . Det fungerar inte för[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) eller[`Table`](../../../aspose.words.tables/table/) noder och noder i sidhuvud/sidfot.

Observera att enheten returnerade för en[`Paragraph`](../../../aspose.words/paragraph/) nod är ett styckebrytningsspann. Använd lämplig metod för att stiga upp till den överordnade raden

Om du behöver navigera till en[`Run`](../../../aspose.words/run/) av text så kan du infoga bokmärke precis före it och sedan navigera till bokmärket istället.

Om du behöver navigera till en[`Cell`](../../../aspose.words.tables/cell/) nod så kan du flytta till en[`Paragraph`](../../../aspose.words/paragraph/) nod i den här cellen och stig sedan upp till en överordnad enhet. Samma tillvägagångssätt kan användas för[`Row`](../../../aspose.words.tables/row/) och[`Table`](../../../aspose.words.tables/table/) knutpunkter.

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

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* namnutrymme [Aspose.Words.Layout](../../layoutcollector/)
* hopsättning [Aspose.Words](../../../)



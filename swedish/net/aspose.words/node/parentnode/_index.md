---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Node ParentNode för att enkelt komma åt den omedelbara föräldern till vilken nod som helst, vilket förbättrar din webbutvecklingseffektivitet och kodtydlighet.
type: docs
weight: 60
url: /sv/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

Hämtar den omedelbara föräldern till denna nod.

```csharp
public CompositeNode ParentNode { get; }
```

## Anmärkningar

Om en nod just har skapats och ännu inte lagts till i trädet, eller om den har tagits bort från trädet, är föräldern`null`.

## Exempel

Visar hur man kommer åt en nods överordnade nod.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Lägg till en underordnad Run-nod till dokumentets första stycke.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// Stycket är den överordnade noden till run-noden. Vi kan spåra denna härstamning
// hela vägen till dokumentnoden, som är roten till dokumentets nodträd.
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

Visar hur man skapar en nod och anger dess ägande dokument.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Vi har ännu inte lagt till detta stycke som ett underordnat stycke till någon sammansatt nod.
Assert.IsNull(para.ParentNode);

// Om en nod är en lämplig undernodtyp till en annan sammansatt nod,
// vi kan bara bifoga den som ett barn om båda noderna har samma ägardokument.
// Ägardokumentet är det dokument vi skickade till nodens konstruktor.
// Vi har inte bifogat detta stycke till dokumentet, så dokumentet innehåller inte dess text.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Eftersom dokumentet äger detta stycke kan vi tillämpa en av dess stilar på styckets innehåll.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Lägg till den här noden i dokumentet och verifiera sedan dess innehåll.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Se även

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

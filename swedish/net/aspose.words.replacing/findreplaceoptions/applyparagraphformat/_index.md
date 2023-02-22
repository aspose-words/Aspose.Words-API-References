---
title: FindReplaceOptions.ApplyParagraphFormat
second_title: Aspose.Words för .NET API Referens
description: FindReplaceOptions fast egendom. Styckeformatering tillämpas på nytt innehåll.
type: docs
weight: 30
url: /sv/net/aspose.words.replacing/findreplaceoptions/applyparagraphformat/
---
## FindReplaceOptions.ApplyParagraphFormat property

Styckeformatering tillämpas på nytt innehåll.

```csharp
public ParagraphFormat ApplyParagraphFormat { get; }
```

### Exempel

Visar hur man lägger till formatering i stycken där en sök-och-ersätt-åtgärd har hittat matchningar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Vi kan använda ett "FindReplaceOptions"-objekt för att ändra sök-och-ersätt-processen.
FindReplaceOptions options = new FindReplaceOptions();

// Ställ in egenskapen "Alignment" till "ParagraphAlignment.Right" för att högerjustera varje stycke
// som innehåller en matchning som hitta-och-ersätt-operationen hittar.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Byt ut varje punkt som är precis före en styckebrytning med ett utropstecken.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Se även

* class [ParagraphFormat](../../../aspose.words/paragraphformat/)
* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../findreplaceoptions/)
* hopsättning [Aspose.Words](../../../)



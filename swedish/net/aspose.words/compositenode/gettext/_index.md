---
title: CompositeNode.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words för .NET
description: Upptäck CompositeNode GetText-metoden för att effektivt hämta text från noder och deras underordnade noder, vilket förbättrar dina databehandlingsmöjligheter.
type: docs
weight: 130
url: /sv/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

Hämtar texten för denna nod och alla dess underordnade noder.

```csharp
public override string GetText()
```

## Anmärkningar

Den returnerade strängen innehåller alla kontroll- och specialtecken enligt beskrivningen i[`ControlChar`](../../controlchar/).

## Exempel

Visar skillnaden mellan att anropa GetText- och ToString-metoderna på en nod.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText hämtar den synliga texten samt fältkoder och specialtecken.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString ger oss dokumentets utseende om det sparas i ett godkänt format.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

Visar hur man skriver ut alla stycken i ett dokument som är listobjekt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Se även

* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

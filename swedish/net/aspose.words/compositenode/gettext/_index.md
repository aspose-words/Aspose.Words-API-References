---
title: CompositeNode.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words för .NET
description: CompositeNode GetText metod. Hämtar texten för denna nod och alla dess underordnade i C#.
type: docs
weight: 110
url: /sv/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

Hämtar texten för denna nod och alla dess underordnade.

```csharp
public override string GetText()
```

## Anmärkningar

Den returnerade strängen innehåller alla kontroll- och specialtecken som beskrivs i[`ControlChar`](../../controlchar/).

## Exempel

Visar skillnaden mellan att anropa GetText- och ToString-metoderna på en nod.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText kommer att hämta den synliga texten samt fältkoder och specialtecken.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString kommer att ge oss dokumentets utseende om det sparas i ett godkänt sparaformat.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Visar hur man matar ut alla stycken i ett dokument som är listobjekt.

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

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Se även

* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

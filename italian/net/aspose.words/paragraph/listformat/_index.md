---
title: Paragraph.ListFormat
second_title: Aspose.Words per .NET API Reference
description: Paragraph proprietà. Fornisce laccesso alle proprietà di formattazione dellelenco del paragrafo.
type: docs
weight: 150
url: /it/net/aspose.words/paragraph/listformat/
---
## Paragraph.ListFormat property

Fornisce l'accesso alle proprietà di formattazione dell'elenco del paragrafo.

```csharp
public ListFormat ListFormat { get; }
```

### Esempi

Mostra come restituire tutti i paragrafi in un documento che sono elementi di elenco.

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

### Guarda anche

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../paragraph/)
* assemblea [Aspose.Words](../../../)



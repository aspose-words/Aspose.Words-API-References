---
title: Paragraph.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà Paragraph ListFormat per accedere facilmente e personalizzare la formattazione dell'elenco dei paragrafi, migliorando la presentazione del tuo documento.
type: docs
weight: 150
url: /it/net/aspose.words/paragraph/listformat/
---
## Paragraph.ListFormat property

Fornisce accesso alle proprietà di formattazione dell'elenco del paragrafo.

```csharp
public ListFormat ListFormat { get; }
```

## Esempi

Mostra come visualizzare tutti i paragrafi di un documento che sono elementi di elenco.

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

### Guarda anche

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

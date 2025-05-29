---
title: List.ListId
linktitle: ListId
articleTitle: ListId
second_title: Aspose.Words per .NET
description: Scopri l'esclusiva proprietà ListId per accedere e gestire facilmente le tue liste. Semplifica il tuo flusso di lavoro con questo identificatore essenziale.
type: docs
weight: 60
url: /it/net/aspose.words.lists/list/listid/
---
## List.ListId property

Ottiene l'identificatore univoco dell'elenco.

```csharp
public int ListId { get; }
```

## Osservazioni

Normalmente non è necessario utilizzare questa proprietà. Ma se la usi, normalmente lo fai insieme a[`GetListByListId`](../../listcollection/getlistbylistid/) metodo per trovare un elenco a tramite il suo identificatore.

## Esempi

Mostra come verificare le proprietà dei documenti proprietari degli elenchi.

```csharp
Document doc = new Document();

ListCollection lists = doc.Lists;
Assert.AreEqual(doc, lists.Document);

List list = lists.Add(ListTemplate.BulletDefault);
Assert.AreEqual(doc, list.Document);

Console.WriteLine("Current list count: " + lists.Count);
Console.WriteLine("Is the first document list: " + (lists[0].Equals(list)));
Console.WriteLine("ListId: " + list.ListId);
Console.WriteLine("List is the same by ListId: " + (lists.GetListByListId(1).Equals(list)));
```

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

* class [List](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)

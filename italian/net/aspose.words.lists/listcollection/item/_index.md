---
title: ListCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente agli elementi di ListCollection tramite indice. Semplifica la gestione dei dati e migliora l'efficienza della tua programmazione con questa potente proprietà!
type: docs
weight: 30
url: /it/net/aspose.words.lists/listcollection/item/
---
## ListCollection indexer

Ottiene un elenco per indice.

```csharp
public List this[int index] { get; }
```

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

Mostra come applicare la formattazione di un elenco esistente a una raccolta di paragrafi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1");
builder.Writeln("Paragraph 2");
builder.Write("Paragraph 3");

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(0, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));

doc.Lists.Add(ListTemplate.NumberDefault);
List docList = doc.Lists[0];

foreach (Paragraph paragraph in paras.OfType<Paragraph>())
{
    paragraph.ListFormat.List = docList;
    paragraph.ListFormat.ListLevelNumber = 2;
}

Assert.AreEqual(3, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));
```

### Guarda anche

* class [List](../../list/)
* class [ListCollection](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)

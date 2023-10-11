---
title: ListCollection.Count
second_title: Aspose.Words per .NET API Reference
description: ListCollection proprietà. Ottiene il conteggio degli elenchi numerati e puntati nel documento.
type: docs
weight: 10
url: /it/net/aspose.words.lists/listcollection/count/
---
## ListCollection.Count property

Ottiene il conteggio degli elenchi numerati e puntati nel documento.

```csharp
public int Count { get; }
```

### Esempi

Mostra come verificare le proprietà del documento proprietario degli elenchi.

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

### Guarda anche

* class [ListCollection](../)
* spazio dei nomi [Aspose.Words.Lists](../../listcollection/)
* assemblea [Aspose.Words](../../../)



---
title: ListCollection.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words per .NET
description: Scopri la proprietà Documento ListCollection per accedere facilmente al documento proprietario e semplificare la gestione dei dati. Ottieni l'efficienza oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.lists/listcollection/document/
---
## ListCollection.Document property

Ottiene il documento del proprietario.

```csharp
public DocumentBase Document { get; }
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

### Guarda anche

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [ListCollection](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)

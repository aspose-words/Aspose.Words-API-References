---
title: ListCollection.GetListByListId
linktitle: GetListByListId
articleTitle: GetListByListId
second_title: Aspose.Words per .NET
description: Recupera l'elenco desiderato senza sforzo con il metodo GetListByListId. Accedi rapidamente ai dati utilizzando un semplice identificatore di elenco per una maggiore efficienza.
type: docs
weight: 80
url: /it/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

Ottiene un elenco tramite un identificatore di elenco.

```csharp
public List GetListByListId(int listId)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| listId | Int32 | Identificatore dell'elenco. |

### Valore di ritorno

Restituisce l'oggetto elenco. Restituisce`null` se non è stato trovato un elenco con l'identificatore specificato.

## Osservazioni

Normalmente non è necessario utilizzare questo metodo. Il più delle volte si applica la formattazione dell'elenco ai paragrafi semplicemente impostando[`List`](../../listformat/list/) proprietà del[`ListFormat`](../../listformat/) oggetto.

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

* class [List](../../list/)
* class [ListCollection](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)

---
title: ListCollection.GetListByListId
linktitle: GetListByListId
articleTitle: GetListByListId
second_title: Aspose.Words för .NET
description: Hämta din önskade lista enkelt med GetListByListId-metoden. Få snabb åtkomst till data med hjälp av en enkel listidentifierare för ökad effektivitet.
type: docs
weight: 80
url: /sv/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

Hämtar en lista med hjälp av en listidentifierare.

```csharp
public List GetListByListId(int listId)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| listId | Int32 | Listidentifieraren. |

### Returvärde

Returnerar listobjektet.`null` om en lista med den angivna identifieraren inte hittades.

## Anmärkningar

Normalt sett behöver du inte använda den här metoden. För det mesta tillämpar du listformatering på stycken bara genom att ställa in[`List`](../../listformat/list/) property av[`ListFormat`](../../listformat/) objekt.

## Exempel

Visar hur man verifierar egenskaper för ägardokument för listor.

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

### Se även

* class [List](../../list/)
* class [ListCollection](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)

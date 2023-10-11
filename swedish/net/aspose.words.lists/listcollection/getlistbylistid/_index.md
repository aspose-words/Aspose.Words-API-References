---
title: ListCollection.GetListByListId
second_title: Aspose.Words för .NET API Referens
description: ListCollection metod. Hämtar en lista med en listidentifierare.
type: docs
weight: 70
url: /sv/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

Hämtar en lista med en listidentifierare.

```csharp
public List GetListByListId(int listId)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| listId | Int32 | Listidentifieraren. |

### Returvärde

Returnerar listobjektet. Returnerar`null` om en lista med den angivna identifieraren inte hittades.

### Anmärkningar

Du behöver normalt inte använda den här metoden. För det mesta tillämpar du listformatting på stycken bara genom att ställa in[`List`](../../listformat/list/) egenskap av[`ListFormat`](../../listformat/) objekt.

### Exempel

Visar hur man verifierar ägardokumentegenskaper för listor.

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
* namnutrymme [Aspose.Words.Lists](../../listcollection/)
* hopsättning [Aspose.Words](../../../)



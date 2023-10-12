---
title: ListCollection.Count
second_title: Référence de l'API Aspose.Words pour .NET
description: ListCollection propriété. Obtient le nombre de listes numérotées et à puces dans le document.
type: docs
weight: 10
url: /fr/net/aspose.words.lists/listcollection/count/
---
## ListCollection.Count property

Obtient le nombre de listes numérotées et à puces dans le document.

```csharp
public int Count { get; }
```

### Exemples

Montre comment vérifier les propriétés du document propriétaire des listes.

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

### Voir également

* class [ListCollection](../)
* espace de noms [Aspose.Words.Lists](../../listcollection/)
* Assemblée [Aspose.Words](../../../)



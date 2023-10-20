---
title: ListCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: ListCollection Count mülk. Belgedeki numaralı ve madde işaretli listelerin sayısını alır C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.lists/listcollection/count/
---
## ListCollection.Count property

Belgedeki numaralı ve madde işaretli listelerin sayısını alır.

```csharp
public int Count { get; }
```

## Örnekler

Listelerin sahip belge özelliklerinin nasıl doğrulanacağını gösterir.

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

### Ayrıca bakınız

* class [ListCollection](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)

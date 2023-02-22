---
title: List.Document
second_title: Aspose.Words for .NET API Referansı
description: List mülk. Sahip belgesini alır.
type: docs
weight: 10
url: /tr/net/aspose.words.lists/list/document/
---
## List.Document property

Sahip belgesini alır.

```csharp
public DocumentBase Document { get; }
```

### Notlar

Bir listenin her zaman bir üst belgesi vardır ve yalnızca o belgenin bağlamında geçerlidir.

### Örnekler

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [List](../)
* ad alanı [Aspose.Words.Lists](../../list/)
* toplantı [Aspose.Words](../../../)



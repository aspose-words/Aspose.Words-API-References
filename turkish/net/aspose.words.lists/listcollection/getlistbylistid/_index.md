---
title: ListCollection.GetListByListId
linktitle: GetListByListId
articleTitle: GetListByListId
second_title: .NET için Aspose.Words
description: GetListByListId metoduyla istediğiniz listeyi zahmetsizce alın. Gelişmiş verimlilik için basit bir liste tanımlayıcısı kullanarak verilere hızla erişin.
type: docs
weight: 80
url: /tr/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

Bir liste tanımlayıcısına göre bir liste alır.

```csharp
public List GetListByListId(int listId)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| listId | Int32 | Liste tanımlayıcısı. |

### Geri dönüş değeri

Liste nesnesini döndürür.`hükümsüz` Belirtilen tanımlayıcıya sahip bir liste bulunamadıysa.

## Notlar

Normalde bu yöntemi kullanmanız gerekmez. Çoğu zaman paragraflara sadece şu ayarları yaparak list formatting uygularsınız:[`List`](../../listformat/list/) property öğesinin[`ListFormat`](../../listformat/) nesne.

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

* class [List](../../list/)
* class [ListCollection](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)

---
title: ListCollection.Document
linktitle: Document
articleTitle: Document
second_title: .NET için Aspose.Words
description: Sahip belgesine kolayca erişmek ve veri yönetiminizi kolaylaştırmak için ListCollection Belge özelliğini keşfedin. Verimliliğin kilidini bugün açın!
type: docs
weight: 20
url: /tr/net/aspose.words.lists/listcollection/document/
---
## ListCollection.Document property

Sahip belgesini alır.

```csharp
public DocumentBase Document { get; }
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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [ListCollection](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)

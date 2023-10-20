---
title: ListCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: ListCollection Item mülk. Dizine göre bir liste alır C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.lists/listcollection/item/
---
## ListCollection indexer

Dizine göre bir liste alır.

```csharp
public List this[int index] { get; }
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

Mevcut bir listenin liste formatının bir paragraf koleksiyonuna nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1");
builder.Writeln("Paragraph 2");
builder.Write("Paragraph 3");

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(0, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));

doc.Lists.Add(ListTemplate.NumberDefault);
List list = doc.Lists[0];

foreach (Paragraph paragraph in paras.OfType<Paragraph>())
{
    paragraph.ListFormat.List = list;
    paragraph.ListFormat.ListLevelNumber = 2;
}

Assert.AreEqual(3, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));
```

### Ayrıca bakınız

* class [List](../../list/)
* class [ListCollection](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)

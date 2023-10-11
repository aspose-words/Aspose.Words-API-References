---
title: List.ListId
second_title: Aspose.Words for .NET API Referansı
description: List mülk. Listenin benzersiz tanımlayıcısını alır.
type: docs
weight: 60
url: /tr/net/aspose.words.lists/list/listid/
---
## List.ListId property

Listenin benzersiz tanımlayıcısını alır.

```csharp
public int ListId { get; }
```

### Notlar

Normalde bu özelliği kullanmanıza gerek yoktur. Ancak eğer onu kullanırsanız, normalde so ile birlikte yaparsınız.[`GetListByListId`](../../listcollection/getlistbylistid/) a listesini tanımlayıcısına göre bulma yöntemi.

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

Bir belgedeki liste öğesi olan tüm paragrafların çıktısının nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Ayrıca bakınız

* class [List](../)
* ad alanı [Aspose.Words.Lists](../../list/)
* toplantı [Aspose.Words](../../../)



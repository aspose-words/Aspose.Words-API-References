---
title: ListCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkel åtkomst till ListCollection-objekt via index. Förenkla din datahantering och förbättra din kodningseffektivitet med den här kraftfulla egenskapen!
type: docs
weight: 30
url: /sv/net/aspose.words.lists/listcollection/item/
---
## ListCollection indexer

Hämtar en lista efter index.

```csharp
public List this[int index] { get; }
```

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

Visar hur man tillämpar listformatering av en befintlig lista på en samling stycken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1");
builder.Writeln("Paragraph 2");
builder.Write("Paragraph 3");

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(0, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));

doc.Lists.Add(ListTemplate.NumberDefault);
List docList = doc.Lists[0];

foreach (Paragraph paragraph in paras.OfType<Paragraph>())
{
    paragraph.ListFormat.List = docList;
    paragraph.ListFormat.ListLevelNumber = 2;
}

Assert.AreEqual(3, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));
```

### Se även

* class [List](../../list/)
* class [ListCollection](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)

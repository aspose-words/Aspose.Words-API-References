---
title: ListCollection.Count
linktitle: Count
second_title: Aspose.Words for .NET API Reference
description: ListCollection Count property. Gets the count of numbered and bulleted lists in the document in C#.
type: docs
weight: 10
url: /net/aspose.words.lists/listcollection/count/
---
## Count property

Gets the count of numbered and bulleted lists in the document.

```csharp
public int Count { get; }
```

## Examples

Shows how to verify owner document properties of lists.

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

### See Also

* class [ListCollection](../)
* namespace [Aspose.Words.Lists](../../listcollection/)
* assembly [Aspose.Words](../../../)

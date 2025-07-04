---
title: ListCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: Discover the ListCollection Count property to easily retrieve the number of numbered and bulleted lists in your document, enhancing your content organization.
type: docs
weight: 10
url: /net/aspose.words.lists/listcollection/count/
---
## ListCollection.Count property

Gets the count of numbered and bulleted lists in the document.

```csharp
public int Count { get; }
```

## Examples

Shows how to verify owner document properties of lists.

```csharp
Document doc = new Document();

ListCollection lists = doc.Lists;
Assert.That(lists.Document, Is.EqualTo(doc));

List list = lists.Add(ListTemplate.BulletDefault);
Assert.That(list.Document, Is.EqualTo(doc));

Console.WriteLine("Current list count: " + lists.Count);
Console.WriteLine("Is the first document list: " + (lists[0].Equals(list)));
Console.WriteLine("ListId: " + list.ListId);
Console.WriteLine("List is the same by ListId: " + (lists.GetListByListId(1).Equals(list)));
```

### See Also

* class [ListCollection](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)

---
title: ListCollection.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: ListCollection Document property. Gets the owner document in C#.
type: docs
weight: 20
url: /net/aspose.words.lists/listcollection/document/
---
## ListCollection.Document property

Gets the owner document.

```csharp
public DocumentBase Document { get; }
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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [ListCollection](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)

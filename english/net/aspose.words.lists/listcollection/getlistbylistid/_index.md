---
title: ListCollection.GetListByListId
linktitle: GetListByListId
articleTitle: GetListByListId
second_title: Aspose.Words for .NET
description: Retrieve your desired list effortlessly with the GetListByListId method. Access data quickly using a simple list identifier for enhanced efficiency.
type: docs
weight: 80
url: /net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

Gets a list by a list identifier.

```csharp
public List GetListByListId(int listId)
```

| Parameter | Type | Description |
| --- | --- | --- |
| listId | Int32 | The list identifier. |

### Return Value

Returns the list object. Returns `null` if a list with the specified identifier was not found.

## Remarks

You don't normally need to use this method. Most of the time you apply list formatting to paragraphs just by settings the [`List`](../../listformat/list/) property of the [`ListFormat`](../../listformat/) object.

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

* class [List](../../list/)
* class [ListCollection](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)

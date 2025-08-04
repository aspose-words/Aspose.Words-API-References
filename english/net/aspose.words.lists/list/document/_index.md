---
title: List.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: Discover how to list document properties and access ownership details effortlessly. Unlock your document management potential today!
type: docs
weight: 10
url: /net/aspose.words.lists/list/document/
---
## List.Document property

Gets the owner document.

```csharp
public DocumentBase Document { get; }
```

## Remarks

A list always has a parent document and is valid only in the context of that document.

## Examples

Shows how to verify owner document properties of lists.

```csharp
Document doc = new Document();

ListCollection lists = doc.Lists;
Assert.That(lists.Document, Is.EqualTo(doc));

List docList = lists.Add(ListTemplate.BulletDefault);
Assert.That(docList.Document, Is.EqualTo(doc));

Console.WriteLine("Current list count: " + lists.Count);
Console.WriteLine("Is the first document list: " + (lists[0].Equals(docList)));
Console.WriteLine("ListId: " + docList.ListId);
Console.WriteLine("List is the same by ListId: " + (lists.GetListByListId(1).Equals(docList)));
```

### See Also

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [List](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)

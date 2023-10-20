---
title: ListCollection.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words für .NET
description: ListCollection Document eigendom. Ruft das Eigentümerdokument ab in C#.
type: docs
weight: 20
url: /de/net/aspose.words.lists/listcollection/document/
---
## ListCollection.Document property

Ruft das Eigentümerdokument ab.

```csharp
public DocumentBase Document { get; }
```

## Beispiele

Zeigt, wie Besitzerdokumenteigenschaften von Listen überprüft werden.

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

### Siehe auch

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [ListCollection](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)

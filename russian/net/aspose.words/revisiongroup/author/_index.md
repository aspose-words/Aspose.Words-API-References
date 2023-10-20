---
title: RevisionGroup.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words для .NET
description: RevisionGroup Author свойство. Получает автора этой группы редакций на С#.
type: docs
weight: 10
url: /ru/net/aspose.words/revisiongroup/author/
---
## RevisionGroup.Author property

Получает автора этой группы редакций.

```csharp
public string Author { get; }
```

## Примеры

Показывает, как распечатать информацию о группе редакций в документе.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### Смотрите также

* class [RevisionGroup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

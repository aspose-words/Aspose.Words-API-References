---
title: RevisionGroup.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words для .NET
description: Откройте для себя свойство RevisionGroup Author, чтобы легко определить автора каждой группы ревизий, повысив эффективность управления документами.
type: docs
weight: 10
url: /ru/net/aspose.words/revisiongroup/author/
---
## RevisionGroup.Author property

Получает автора этой группы ревизий.

```csharp
public string Author { get; }
```

## Примеры

Показывает, как распечатать информацию о группе ревизий в документе.

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

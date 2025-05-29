---
title: RevisionGroup.RevisionType
linktitle: RevisionType
articleTitle: RevisionType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство RevisionGroup RevisionType, чтобы легко определять и управлять типами ревизий в вашем проекте. Оптимизируйте свой рабочий процесс сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

Получает тип ревизий, включенных в эту группу.

```csharp
public RevisionType RevisionType { get; }
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

* enum [RevisionType](../../revisiontype/)
* class [RevisionGroup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

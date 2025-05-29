---
title: RevisionGroup Class
linktitle: RevisionGroup
articleTitle: RevisionGroup
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.RevisionGroup, предназначенный для эффективного управления и организации последовательных объектов Revision для упрощенного редактирования документов.
type: docs
weight: 5520
url: /ru/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Представляет группу последовательных[`Revision`](../revision/) объекты.

Чтобы узнать больше, посетите[Отслеживание изменений в документе](https://docs.aspose.com/words/net/track-changes-in-a-document/) документальная статья.

```csharp
public class RevisionGroup
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Получает автора этой группы ревизий. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Получает тип ревизий, включенных в эту группу. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Возвращает вставленный/удаленный/перемещенный текст или описание изменения формата. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)

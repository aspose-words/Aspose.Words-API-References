---
title: Class RevisionGroup
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.RevisionGroup сорт. Представляет группу последовательныхRevision объекты.
type: docs
weight: 4780
url: /ru/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Представляет группу последовательных[`Revision`](../revision/) объекты.

Чтобы узнать больше, посетите[Отслеживать изменения в документе](https://docs.aspose.com/words/net/track-changes-in-a-document/) статья документации.

```csharp
public class RevisionGroup
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Получает автора этой группы редакций. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Получает тип редакций, включенных в эту группу. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Возвращает вставленный/удаленный/перемещенный текст или описание изменения формата. |

### Примеры

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)



---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: Aspose.Words для .NET
description: Aspose.Words.RevisionGroupCollection сорт. КоллекцияRevisionGroup объекты которые представляют группы редакций в документе на С#.
type: docs
weight: 4790
url: /ru/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

Коллекция[`RevisionGroup`](../revisiongroup/) объекты, которые представляют группы редакций в документе.

Чтобы узнать больше, посетите[Отслеживать изменения в документе](https://docs.aspose.com/words/net/track-changes-in-a-document/) статья документации.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | Возвращает количество групп редакций в коллекции. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | Возвращает группу редакций по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | Возвращает объект перечислителя. |

## Примечания

Вы не создаете экземпляры этого класса напрямую. Использовать[`Groups`](../revisioncollection/groups/) Свойство для получения групп редакций, присутствующих в документе.

## Примеры

Показывает, как получить группу редакций в документе.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

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

* class [RevisionGroup](../revisiongroup/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)

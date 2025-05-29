---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.RevisionGroupCollection, обеспечивающий эффективное управление группами редакций документов для расширенного редактирования и совместной работы.
type: docs
weight: 5530
url: /ru/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

Коллекция[`RevisionGroup`](../revisiongroup/)объекты, представляющие группы ревизий в документе.

Чтобы узнать больше, посетите[Отслеживание изменений в документе](https://docs.aspose.com/words/net/track-changes-in-a-document/) документальная статья.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | Возвращает количество групп ревизий в коллекции. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | Возвращает группу ревизий по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | Возвращает объект перечислителя. |

## Примечания

Вы не создаете экземпляры этого класса напрямую. Используйте[`Groups`](../revisioncollection/groups/) Свойство для получения групп ревизий, присутствующих в документе.

## Примеры

Показывает, как получить группу правок в документе.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

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

* class [RevisionGroup](../revisiongroup/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)

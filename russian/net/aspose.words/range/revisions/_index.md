---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: Aspose.Words для .NET
description: Range Revisions свойство. Получает коллекцию редакций отслеживаемых изменений существующих в этом диапазоне на С#.
type: docs
weight: 40
url: /ru/net/aspose.words/range/revisions/
---
## Range.Revisions property

Получает коллекцию редакций (отслеживаемых изменений), существующих в этом диапазоне.

```csharp
public RevisionCollection Revisions { get; }
```

## Примечания

Возвращенная коллекция является «живой» коллекцией, что означает, что если вы удалите части документа, содержащие версии , удаленные версии автоматически исчезнут из этой коллекции.

## Примеры

Показывает, как работать с редакциями в диапазоне.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// Отклоняем первые версии раздела.
doc.FirstSection.Range.Revisions.RejectAll();
```

### Смотрите также

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: Aspose.Words для .NET
description: Откройте для себя Range Revisions. Отслеживайте и управляйте изменениями в недвижимости без усилий с помощью нашей полной коллекции ревизий для повышения ясности проекта.
type: docs
weight: 40
url: /ru/net/aspose.words/range/revisions/
---
## Range.Revisions property

Получает коллекцию ревизий (отслеживаемых изменений), которые существуют в этом диапазоне.

```csharp
public RevisionCollection Revisions { get; }
```

## Примечания

Возвращаемая коллекция является «живой» коллекцией, что означает, что если вы удалите части документа, содержащие ревизий, удаленные ревизии автоматически исчезнут из этой коллекции.

## Примеры

Показывает, как работать с изменениями в диапазоне.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// Отклонить изменения первого раздела.
doc.FirstSection.Range.Revisions.RejectAll();
```

### Смотрите также

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

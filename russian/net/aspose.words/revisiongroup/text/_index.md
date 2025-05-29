---
title: RevisionGroup.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: Изучите свойство RevisionGroup Text для доступа к вставленному, удаленному или перемещенному тексту, что позволит улучшить понимание форматирования документа и эффективность редактирования.
type: docs
weight: 30
url: /ru/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

Возвращает вставленный/удаленный/перемещенный текст или описание изменения формата.

```csharp
public string Text { get; }
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

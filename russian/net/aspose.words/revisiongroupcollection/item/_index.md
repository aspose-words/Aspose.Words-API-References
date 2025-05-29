---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Получите доступ к определенным группам ревизий без усилий с помощью свойства RevisionGroupCollection Item. Улучшите управление данными с помощью точного индексирования.
type: docs
weight: 20
url: /ru/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Возвращает группу ревизий по указанному индексу.

```csharp
public RevisionGroup this[int index] { get; }
```

## Примеры

Показывает, как получить группу правок в документе.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Смотрите также

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: RevisionGroupCollection Item свойство. Возвращает группу редакций по указанному индексу на С#.
type: docs
weight: 20
url: /ru/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Возвращает группу редакций по указанному индексу.

```csharp
public RevisionGroup this[int index] { get; }
```

## Примеры

Показывает, как получить группу редакций в документе.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Смотрите также

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

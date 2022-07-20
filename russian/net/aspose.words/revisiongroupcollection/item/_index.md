---
title: Item
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает группу ревизий по указанному индексу.
type: docs
weight: 20
url: /ru/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

Возвращает группу ревизий по указанному индексу.

```csharp
public RevisionGroup this[int index] { get; }
```

### Примеры

Показывает, как получить группу редакций в документе.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### Смотрите также

* class [RevisionGroup](../../revisiongroup)
* class [RevisionGroupCollection](../../revisiongroupcollection)
* пространство имен [Aspose.Words](../../revisiongroupcollection)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
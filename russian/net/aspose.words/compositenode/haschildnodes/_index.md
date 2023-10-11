---
title: CompositeNode.HasChildNodes
second_title: Справочник по API Aspose.Words для .NET
description: CompositeNode свойство. Возвращаетистинный если у этого узла есть дочерние узлы.
type: docs
weight: 30
url: /ru/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Возвращает`истинный` если у этого узла есть дочерние узлы.

```csharp
public bool HasChildNodes { get; }
```

### Примеры

Показывает, как объединить строки из двух таблиц в одну.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Ниже приведены два способа получения таблицы из документа.
// 1 — Из коллекции «Таблицы» узла Body:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Использование метода "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Добавляем все строки из текущей таблицы в следующую.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Удаляем пустой контейнер таблицы.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Смотрите также

* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../compositenode/)
* сборка [Aspose.Words](../../../)



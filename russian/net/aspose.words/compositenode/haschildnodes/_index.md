---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: Aspose.Words для .NET
description: Узнайте, есть ли у CompositeNode дочерние узлы со свойством HasChildNodes. Упростите кодирование с помощью этой важной функции для эффективного управления узлами.
type: docs
weight: 30
url: /ru/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Возврат`истинный` если у этого узла есть дочерние узлы.

```csharp
public bool HasChildNodes { get; }
```

## Примеры

Показывает, как объединить строки из двух таблиц в одну.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Ниже приведены два способа получения таблицы из документа.
// 1 - Из коллекции "Таблицы" узла Body:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Использование метода "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Добавить все строки из текущей таблицы в следующую.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Удаляем пустой контейнер таблицы.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Смотрите также

* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

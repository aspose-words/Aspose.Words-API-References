---
title: CellFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CellFormat Borders, чтобы получить доступ к коллекциям границ ячеек и настроить их для улучшения дизайна и функциональности электронных таблиц.
type: docs
weight: 10
url: /ru/net/aspose.words.tables/cellformat/borders/
---
## CellFormat.Borders property

Получает коллекцию границ ячейки.

```csharp
public BorderCollection Borders { get; }
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

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [CellFormat](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)

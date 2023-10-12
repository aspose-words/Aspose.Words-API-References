---
title: CellFormat.ClearFormatting
second_title: Справочник по API Aspose.Words для .NET
description: CellFormat метод. Сбрасывает формат ячейки по умолчанию. Не меняет ширину ячейки.
type: docs
weight: 160
url: /ru/net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

Сбрасывает формат ячейки по умолчанию. Не меняет ширину ячейки.

```csharp
public void ClearFormatting()
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

* class [CellFormat](../)
* пространство имен [Aspose.Words.Tables](../../cellformat/)
* сборка [Aspose.Words](../../../)



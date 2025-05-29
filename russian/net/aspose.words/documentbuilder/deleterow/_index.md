---
title: DocumentBuilder.DeleteRow
linktitle: DeleteRow
articleTitle: DeleteRow
second_title: Aspose.Words для .NET
description: Легко удаляйте строки из таблиц с помощью метода DocumentBuilder DeleteRow. Оптимизируйте редактирование документов и улучшите свой рабочий процесс!
type: docs
weight: 200
url: /ru/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

Удаляет строку из таблицы.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| tableIndex | Int32 | Индекс таблицы. |
| rowIndex | Int32 | Индекс строки в таблице. |

### Возвращаемое значение

Узел строки, который был только что удален.

## Примечания

Если курсор находится внутри удаляемой строки, он перемещается наружу на следующую строку или на следующий абзац после таблицы.

Если удалить строку из таблицы, содержащей только одну строку, вся таблица whole будет удалена.

Для параметров индекса, когда index больше или равен 0, он указывает индекс from в начале, где 0 является первым элементом. Когда index меньше 0, он указывает индекс from в конце, где -1 является последним элементом.

## Примеры

Показывает, как удалить строку из таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.Write("Row 2, cell 2.");
builder.EndTable();

Assert.AreEqual(2, table.Rows.Count);

// Удаляем первую строку первой таблицы в документе.
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### Смотрите также

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

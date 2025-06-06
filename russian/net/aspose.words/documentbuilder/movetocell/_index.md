---
title: DocumentBuilder.MoveToCell
linktitle: MoveToCell
articleTitle: MoveToCell
second_title: Aspose.Words для .NET
description: Легко перемещайтесь по документу с помощью метода MoveToCell в DocumentBuilder, быстро устанавливая курсор в любую ячейку таблицы для расширенного редактирования.
type: docs
weight: 540
url: /ru/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

Перемещает курсор в ячейку таблицы в текущем разделе.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| tableIndex | Int32 | Индекс таблицы, к которой необходимо перейти. |
| rowIndex | Int32 | Индекс строки в таблице. |
| columnIndex | Int32 | Индекс столбца в таблице. |
| characterIndex | Int32 | Индекс символа внутри ячейки. Отрицательное значение позволяет указать позицию от конца ячейки. Используйте -1 для перемещения в конец ячейки. |

## Примечания

Навигация осуществляется внутри текущей истории текущего раздела.

Для параметров индекса, когда index больше или равен 0, он указывает индекс from в начале, где 0 является первым элементом. Когда index меньше 0, он указывает индекс from в конце, где -1 является последним элементом.

## Примеры

Показывает, как переместить курсор конструктора документов в ячейку таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем пустую таблицу 2x2.
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// Поскольку мы завершили таблицу методом EndTable,
// курсор конструктора документов в данный момент находится за пределами таблицы.
// Этот курсор имеет ту же функцию, что и мигающий текстовый курсор Microsoft Word.
// Его также можно переместить в другое место документа с помощью методов MoveTo конструктора.
// Мы можем переместить курсор обратно в таблицу в определенную ячейку.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

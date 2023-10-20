---
title: Table.AutoFit
linktitle: AutoFit
articleTitle: AutoFit
second_title: Aspose.Words для .NET
description: Table AutoFit метод. Изменяет размеры таблицы и ячеек в соответствии с указанным поведением автоподбора на С#.
type: docs
weight: 360
url: /ru/net/aspose.words.tables/table/autofit/
---
## Table.AutoFit method

Изменяет размеры таблицы и ячеек в соответствии с указанным поведением автоподбора.

```csharp
public void AutoFit(AutoFitBehavior behavior)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| behavior | AutoFitBehavior | Указывает, как автоматически подогнать таблицу. |

## Примечания

Этот метод имитирует команды, доступные в меню «Автоматическое размещение» для таблицы в Microsoft Word. Доступные команды: «Автоматическое соответствие содержимому», «Автоматическое соответствие размеру окна» и «Фиксированная ширина столбца». В Microsoft Word эти команды устанавливают соответствующие свойства таблицы, а затем обновляют макет таблицы, и Aspose.Words делает то же самое за вас.

## Примеры

Показывает, как построить новую таблицу с применением стиля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Мы должны вставить хотя бы одну строку, прежде чем устанавливать какое-либо форматирование таблицы.
builder.InsertCell();

// Установите используемый стиль таблицы на основе идентификатора стиля.
// Обратите внимание, что не все стили таблиц доступны при сохранении в формате .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Частично применить стиль к функциям таблицы на основе предикатов, затем построить таблицу.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### Смотрите также

* enum [AutoFitBehavior](../../autofitbehavior/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)

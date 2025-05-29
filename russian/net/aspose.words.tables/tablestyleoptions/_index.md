---
title: TableStyleOptions Enum
linktitle: TableStyleOptions
articleTitle: TableStyleOptions
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Tables.TableStyleOptions для гибкого оформления таблиц. Улучшите дизайн вашего документа с помощью настраиваемых стилей таблиц уже сегодня!
type: docs
weight: 7220
url: /ru/net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

Указывает, как стиль таблицы применяется к таблице.

```csharp
[Flags]
public enum TableStyleOptions
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Форматирование стиля таблицы не применяется. |
| FirstRow | `20` | Применить условное форматирование первой строки. |
| LastRow | `40` | Применить условное форматирование последней строки. |
| FirstColumn | `80` | Применить условное форматирование к 1 первому столбцу. |
| LastColumn | `100` | Применить условное форматирование последнего столбца. |
| RowBands | `200` | Применить условное форматирование полосы строк. |
| ColumnBands | `400` | Применить условное форматирование полосы столбцов. |
| Default2003 | `600` | Применяется полоса строк и столбцов. Это значение по умолчанию Microsoft Word для старых форматов, таких как DOC, WML и RTF. |
| Default | `2A0` | Это настройки Microsoft Word по умолчанию. |

## Примеры

Показывает, как создать новую таблицу, применяя стиль.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Перед настройкой форматирования таблицы необходимо вставить хотя бы одну строку.
builder.InsertCell();

// Устанавливаем используемый стиль таблицы на основе идентификатора стиля.
// Обратите внимание, что не все стили таблиц доступны при сохранении в формате .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Частично применяем стиль к признакам таблицы на основе предикатов, затем создаем таблицу.
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

* property [StyleOptions](../table/styleoptions/)
* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)

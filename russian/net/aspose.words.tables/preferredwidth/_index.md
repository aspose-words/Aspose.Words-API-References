---
title: PreferredWidth Class
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Tables.PreferredWidth, ваше решение для определения оптимальной ширины таблиц и ячеек с точностью и гибкостью. Улучшите макеты своих документов сегодня!
type: docs
weight: 7140
url: /ru/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

Представляет значение и его единицу измерения, которые используются для указания предпочтительной ширины таблицы или ячейки.

Чтобы узнать больше, посетите[Работа с таблицами](https://docs.aspose.com/words/net/working-with-tables/) документальная статья.

```csharp
public sealed class PreferredWidth
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | Получает единицу измерения, используемую для этого предпочтительного значения ширины. |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | Получает предпочтительное значение ширины. Единица измерения указана в[`Type`](./type/) свойство. |

## Методы

| Имя | Описание |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(*double*) | Метод создания, который возвращает новый экземпляр, представляющий предпочтительную ширину, указанную в процентах. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(*double*) | Метод создания, который возвращает новый экземпляр, представляющий предпочтительную ширину, указанную с использованием ряда точек. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(*object*) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(*PreferredWidth*) | Определяет, является ли указанный`PreferredWidth` равен по значению текущему`PreferredWidth` . |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | Служит хэш-функцией для этого типа. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | Возвращает удобную для пользователя строку, отображающую значение этого объекта. |

## Поля

| Имя | Описание |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | Возвращает экземпляр, представляющий значение «предпочтительная ширина не указана». |

## Примечания

Предпочтительную ширину можно указать в процентах, количестве точек или в виде специального значения «нет/авто».

Экземпляры этого класса неизменяемы.

## Примеры

Показывает, как настроить автоматическое подгонку таблицы под ширину страницы (50%).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

Показывает, как установить предпочтительную ширину ячеек таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Существует два способа применения класса «PreferredWidth» к ячейкам таблицы.
// 1 — Установить абсолютную предпочтительную ширину на основе точек:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Установить относительную предпочтительную ширину на основе процента от ширины таблицы:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Ячейка, для которой не указана предпочтительная ширина, займет оставшееся доступное пространство.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Каждая конфигурация свойства «PreferredWidth» создает новый объект.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)

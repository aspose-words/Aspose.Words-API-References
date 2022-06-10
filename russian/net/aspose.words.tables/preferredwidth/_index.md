---
title: PreferredWidth
second_title: Справочник по API Aspose.Words для .NET
description: Представляет значение и его единицу измерения которые используются для указания предпочтительной ширины таблицы или ячейки.
type: docs
weight: 5940
url: /ru/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

Представляет значение и его единицу измерения, которые используются для указания предпочтительной ширины таблицы или ячейки.

```csharp
public sealed class PreferredWidth
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type) { get; } | Получает единицу измерения, используемую для этого предпочтительного значения ширины. |
| [Value](../../aspose.words.tables/preferredwidth/value) { get; } | Получает предпочтительное значение ширины. Единица измерения указывается в свойстве[`Type`](./type). |

## Методы

| Имя | Описание |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent)(double) | Метод создания, который возвращает новый экземпляр, представляющий предпочтительную ширину, указанную в процентах. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints)(double) | Метод создания, который возвращает новый экземпляр, представляющий предпочтительную ширину, указанную с использованием количества точек. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals#equals_1)(object) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [Equals](../../aspose.words.tables/preferredwidth/equals#equals)(PreferredWidth) | Определяет, равна ли указанная PreferredWidth по значению текущей PreferredWidth. |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode)() | Служит хеш-функцией для этого типа. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring)() | Возвращает удобную для пользователя строку, отображающую значение этого объекта. |

## Поля

| Имя | Описание |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto) | Возвращает экземпляр, представляющий значение "предпочтительная ширина не указана". |

### Примечания

Предпочтительная ширина может быть указана в процентах, количестве точек или специальном "none/auto". " ценность.

Экземпляры этого класса неизменяемы.

### Примеры

Показывает, как настроить таблицу для автоматического заполнения до 50% ширины страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Существует два способа применения класса PreferredWidth к ячейкам таблицы.
// 1 - Установить абсолютную предпочтительную ширину в пунктах:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Установите относительную предпочтительную ширину в процентах от ширины таблицы:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Ячейка, для которой не указана предпочтительная ширина, займет оставшееся доступное пространство.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Каждая конфигурация свойства PreferredWidth создает новый объект.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

Показывает, как установить предпочтительную ширину для ячеек таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Существует два способа применения класса PreferredWidth к ячейкам таблицы.
// 1 - Установить абсолютную предпочтительную ширину в пунктах:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Установите относительную предпочтительную ширину в процентах от ширины таблицы:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Ячейка, для которой не указана предпочтительная ширина, займет оставшееся доступное пространство.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Каждая конфигурация свойства PreferredWidth создает новый объект.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Смотрите также

* namespace [Aspose.Words.Tables](../../aspose.words.tables)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->

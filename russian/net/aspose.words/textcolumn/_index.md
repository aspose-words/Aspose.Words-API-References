---
title: TextColumn Class
linktitle: TextColumn
articleTitle: TextColumn
second_title: Aspose.Words для .NET
description: Aspose.Words.TextColumn сорт. Представляет один текстовый столбец.TextColumn является членомTextColumnCollection коллекция. TextColumn коллекция включает в себя все столбцы раздела документа на С#.
type: docs
weight: 6390
url: /ru/net/aspose.words/textcolumn/
---
## TextColumn class

Представляет один текстовый столбец.`TextColumn` является членом[`TextColumnCollection`](../textcolumncollection/) коллекция. `TextColumn` коллекция включает в себя все столбцы раздела документа.

Чтобы узнать больше, посетите[Работа с разделами](https://docs.aspose.com/words/net/working-with-sections/) статья документации.

```csharp
public class TextColumn
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Получает или задает расстояние между этим столбцом и следующим столбцом в пунктах. Не требуется для последнего столбца. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Получает или задает ширину текстового столбца в пунктах. |

## Примечания

`TextColumn` объекты используются только для указания столбцов с произвольной шириной и интервалом. Если вы хотите столбцы в документе иметь одинаковую ширину, установите TextColumns.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) к`истинный`.

Когда новый`TextColumn` создается, его ширина и интервал установлены на ноль.

## Примеры

Показывает, как создавать столбцы с неравномерным расположением друг от друга.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Определим количество свободного места для размещения столбцов.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Установите узкий первый столбец.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Установите второй столбец так, чтобы он занял оставшееся пространство, доступное в пределах полей страницы.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)

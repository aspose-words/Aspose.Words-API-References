---
title: TextColumn Class
linktitle: TextColumn
articleTitle: TextColumn
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.TextColumn для управления текстовыми столбцами в ваших документах. Легко получайте доступ и настраивайте каждый столбец в вашем текстовом разделе.
type: docs
weight: 7240
url: /ru/net/aspose.words/textcolumn/
---
## TextColumn class

Представляет один текстовый столбец.`TextColumn` является членом[`TextColumnCollection`](../textcolumncollection/) коллекция. `TextColumn`коллекция включает в себя все столбцы в разделе документа.

Чтобы узнать больше, посетите[Работа с разделами](https://docs.aspose.com/words/net/working-with-sections/) документальная статья.

```csharp
public class TextColumn
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Получает или задает расстояние между этим столбцом и следующим столбцом в точках. Не требуется для последнего столбца. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Возвращает или задает ширину текстового столбца в пунктах. |

## Примечания

`TextColumn` объекты используются только для указания столбцов с пользовательской шириной и интервалом. Если вы хотите, чтобы столбцы в документе были одинаковой ширины, установите TextColumns.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) к`истинный`.

Когда новый`TextColumn` при создании его ширина и интервал устанавливаются равными нулю.

## Примеры

Показывает, как создавать неравномерно расположенные столбцы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Определяем количество места, доступного для размещения столбцов.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Сделаем первый столбец узким.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Установите второй столбец так, чтобы он занимал оставшееся пространство на полях страницы.
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

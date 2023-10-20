---
title: ConvertUtil Class
linktitle: ConvertUtil
articleTitle: ConvertUtil
second_title: Aspose.Words для .NET
description: Aspose.Words.ConvertUtil сорт. Предоставляет вспомогательные функции для преобразования различных единиц измерения на С#.
type: docs
weight: 360
url: /ru/net/aspose.words/convertutil/
---
## ConvertUtil class

Предоставляет вспомогательные функции для преобразования различных единиц измерения.

Чтобы узнать больше, посетите[Преобразование между единицами измерения](https://docs.aspose.com/words/net/convert-between-measurement-units/) статья документации.

```csharp
public static class ConvertUtil
```

## Методы

| Имя | Описание |
| --- | --- |
| static [InchToPoint](../../aspose.words/convertutil/inchtopoint/)(*double*) | Преобразует дюймы в пункты. |
| static [MillimeterToPoint](../../aspose.words/convertutil/millimetertopoint/)(*double*) | Преобразует миллиметры в точки. |
| static [PixelToNewDpi](../../aspose.words/convertutil/pixeltonewdpi/)(*double, double, double*) | Преобразует пиксели из одного разрешения в другое. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint)(*double*) | Преобразует пиксели в точки с разрешением 96 точек на дюйм. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint_1)(*double, double*) | Преобразует пиксели в точки с указанным разрешением в пикселях. |
| static [PointToInch](../../aspose.words/convertutil/pointtoinch/)(*double*) | Преобразует точки в дюймы. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel)(*double*) | Преобразует точки в пиксели с разрешением 96 точек на дюйм. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel_1)(*double, double*) | Преобразует точки в пиксели с указанным разрешением в пикселях. |

## Примеры

Показывает, как настроить размер бумаги, ориентацию, поля и другие параметры раздела.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Показывает, как указать свойства страницы в дюймах.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Параметр «Параметры страницы» раздела определяет размер полей страницы в пунктах.
// Мы также можем использовать класс ConvertUtil для использования более знакомой единицы измерения,
// например, дюймы при определении границ.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// Дюйм — 72 пункта.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Добавляем контент, чтобы продемонстрировать новые поля.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)

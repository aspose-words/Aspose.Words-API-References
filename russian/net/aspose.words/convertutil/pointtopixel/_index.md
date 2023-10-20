---
title: ConvertUtil.PointToPixel
linktitle: PointToPixel
articleTitle: PointToPixel
second_title: Aspose.Words для .NET
description: ConvertUtil PointToPixel метод. Преобразует точки в пиксели с разрешением 96 точек на дюйм на С#.
type: docs
weight: 60
url: /ru/net/aspose.words/convertutil/pointtopixel/
---
## PointToPixel(*double*) {#pointtopixel}

Преобразует точки в пиксели с разрешением 96 точек на дюйм.

```csharp
public static double PointToPixel(double points)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| points | Double | Значение для преобразования. |

## Примечания

1 дюйм равен 72 баллам.

## Примеры

Показывает, как указать свойства страницы в пикселях.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Параметр «Параметры страницы» раздела определяет размер полей страницы в пунктах.
// Мы также можем использовать класс ConvertUtil для использования другой единицы измерения,
// например, пиксели при определении границ.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100);
pageSetup.BottomMargin = ConvertUtil.PixelToPoint(200);
pageSetup.LeftMargin = ConvertUtil.PixelToPoint(225);
pageSetup.RightMargin = ConvertUtil.PixelToPoint(125);

// Пиксель — это 0,75 пункта.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToPixel(0.75));

// Используемое значение DPI по умолчанию — 96.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1, 96));

// Добавляем контент, чтобы продемонстрировать новые поля.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToPixel(pageSetup.LeftMargin)} pixels from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToPixel(pageSetup.RightMargin)} pixels from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin)} pixels from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToPixel(pageSetup.BottomMargin)} pixels from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixels.docx");
```

### Смотрите также

* class [ConvertUtil](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## PointToPixel(*double, double*) {#pointtopixel_1}

Преобразует точки в пиксели с указанным разрешением в пикселях.

```csharp
public static double PointToPixel(double points, double resolution)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| points | Double | Значение для преобразования. |
| resolution | Double | Разрешение dpi (точек на дюйм). |

## Примечания

1 дюйм равен 72 баллам.

## Примеры

Показывает, как использовать преобразование точек в пиксели с разрешением по умолчанию и пользовательским разрешением.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Определите размер верхнего поля этого раздела в пикселях в соответствии с пользовательским разрешением.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// При разрешении по умолчанию, равном 96, пиксель составляет 0,75 пункта.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// Установите новое значение DPI и соответствующим образом отрегулируйте значение верхнего поля.
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.AreEqual(59.0d, pageSetup.TopMargin, 0.01d);

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### Смотрите также

* class [ConvertUtil](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

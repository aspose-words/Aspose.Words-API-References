---
title: ConvertUtil.PixelToNewDpi
linktitle: PixelToNewDpi
articleTitle: PixelToNewDpi
second_title: Aspose.Words для .NET
description: ConvertUtil PixelToNewDpi метод. Преобразует пиксели из одного разрешения в другое на С#.
type: docs
weight: 30
url: /ru/net/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil.PixelToNewDpi method

Преобразует пиксели из одного разрешения в другое.

```csharp
public static int PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pixels | Double | Значение для преобразования. |
| oldDpi | Double | Текущее разрешение dpi (точек на дюйм). |
| newDpi | Double | Новое разрешение dpi (точек на дюйм). |

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

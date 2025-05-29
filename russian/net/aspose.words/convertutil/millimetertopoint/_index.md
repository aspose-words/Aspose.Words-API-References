---
title: ConvertUtil.MillimeterToPoint
linktitle: MillimeterToPoint
articleTitle: MillimeterToPoint
second_title: Aspose.Words для .NET
description: Легко конвертируйте миллиметры в точки с помощью метода MillimeterToPoint от ConvertUtil. Упростите свои расчеты дизайна сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method

Преобразует миллиметры в точки.

```csharp
public static double MillimeterToPoint(double millimeters)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| millimeters | Double | Значение для преобразования. |

## Примечания

1 дюйм равен 25,4 миллиметра. 1 дюйм равен 72 точкам.

## Примеры

Показывает, как указать свойства страницы в миллиметрах.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// «Параметры страницы» раздела определяют размер полей страницы в пунктах.
// Мы также можем использовать класс «ConvertUtil» для использования более привычной единицы измерения,
// например миллиметры при определении границ.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.MillimeterToPoint(30);
pageSetup.BottomMargin = ConvertUtil.MillimeterToPoint(50);
pageSetup.LeftMargin = ConvertUtil.MillimeterToPoint(80);
pageSetup.RightMargin = ConvertUtil.MillimeterToPoint(40);

// Сантиметр равен примерно 28,3 пункта.
Assert.AreEqual(28.34d, ConvertUtil.MillimeterToPoint(10), 0.01d);

// Добавьте контент для демонстрации новых полей.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points from the left, " +
                $"{pageSetup.RightMargin} points from the right, " +
                $"{pageSetup.TopMargin} points from the top, " +
                $"and {pageSetup.BottomMargin} points from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### Смотрите также

* class [ConvertUtil](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

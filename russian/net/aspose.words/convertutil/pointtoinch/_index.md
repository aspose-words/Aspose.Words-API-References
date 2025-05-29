---
title: ConvertUtil.PointToInch
linktitle: PointToInch
articleTitle: PointToInch
second_title: Aspose.Words для .NET
description: Легко конвертируйте точки в дюймы с помощью метода PointToInch от ConvertUtil. Упростите свои измерения и повысьте точность своего дизайна уже сегодня!
type: docs
weight: 50
url: /ru/net/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil.PointToInch method

Преобразует точки в дюймы.

```csharp
public static double PointToInch(double points)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| points | Double | Значение для преобразования. |

## Примечания

1 дюйм равен 72 точкам.

## Примеры

Показывает, как указать свойства страницы в дюймах.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// «Параметры страницы» раздела определяют размер полей страницы в пунктах.
// Мы также можем использовать класс «ConvertUtil» для использования более привычной единицы измерения,
// например, дюймы при определении границ.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// Дюйм — это 72 пункта.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Добавьте контент для демонстрации новых полей.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Смотрите также

* class [ConvertUtil](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

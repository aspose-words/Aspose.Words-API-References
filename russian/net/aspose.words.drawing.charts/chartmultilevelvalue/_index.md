---
title: ChartMultilevelValue Class
linktitle: ChartMultilevelValue
articleTitle: ChartMultilevelValue
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.ChartMultilevelValue для эффективного управления многоуровневыми данными в ваших диаграммах, расширяя возможности визуализации данных.
type: docs
weight: 1050
url: /ru/net/aspose.words.drawing.charts/chartmultilevelvalue/
---
## ChartMultilevelValue class

Представляет значение для диаграмм, отображающих многоуровневые данные.

```csharp
public class ChartMultilevelValue
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor)(*string*) | Инициализирует новый экземпляр этого класса, представляющий одноуровневое значение. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_1)(*string, string*) | Инициализирует новый экземпляр этого класса, представляющий двухуровневое значение. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_2)(*string, string, string*) | Инициализирует новый экземпляр этого класса, представляющий трехуровневое значение. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Level1](../../aspose.words.drawing.charts/chartmultilevelvalue/level1/) { get; } | Получает имя верхнего уровня диаграммы, к которому относится это значение. |
| [Level2](../../aspose.words.drawing.charts/chartmultilevelvalue/level2/) { get; } | Получает имя промежуточного уровня диаграммы, к которому относится это значение. |
| [Level3](../../aspose.words.drawing.charts/chartmultilevelvalue/level3/) { get; } | Получает имя нижнего уровня диаграммы, к которому относится это значение. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/chartmultilevelvalue/equals/)(*object*) | Возвращает флаг, указывающий, равен ли указанный объект текущему многоуровневому объекту данных. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartmultilevelvalue/gethashcode/)() | Получает хэш-код для текущего многоуровневого объекта данных. |

## Примеры

Показывает, как создать древовидную диаграмму.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить диаграмму Treemap.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

// Добавить серию.
ChartSeries series = chart.Series.Add(
    "Population by Region",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Asia", "China"),
        new ChartMultilevelValue("Asia", "India"),
        new ChartMultilevelValue("Asia", "Indonesia"),
        new ChartMultilevelValue("Asia", "Pakistan"),
        new ChartMultilevelValue("Asia", "Bangladesh"),
        new ChartMultilevelValue("Asia", "Japan"),
        new ChartMultilevelValue("Asia", "Philippines"),
        new ChartMultilevelValue("Asia", "Other"),
        new ChartMultilevelValue("Africa", "Nigeria"),
        new ChartMultilevelValue("Africa", "Ethiopia"),
        new ChartMultilevelValue("Africa", "Egypt"),
        new ChartMultilevelValue("Africa", "Other"),
        new ChartMultilevelValue("Europe", "Russia"),
        new ChartMultilevelValue("Europe", "Germany"),
        new ChartMultilevelValue("Europe", "Other"),
        new ChartMultilevelValue("Latin America", "Brazil"),
        new ChartMultilevelValue("Latin America", "Mexico"),
        new ChartMultilevelValue("Latin America", "Other"),
        new ChartMultilevelValue("Northern America", "United States", "Other"),
        new ChartMultilevelValue("Northern America", "Other"),
        new ChartMultilevelValue("Oceania")
    },
    new double[]
    {
        1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000,
        223800000, 107334000, 105914499, 903000000,
        146150789, 84607016, 516000000,
        203080756, 129713690, 310000000,
        335893238, 35000000,
        42000000
    });

// Показать метки данных.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)

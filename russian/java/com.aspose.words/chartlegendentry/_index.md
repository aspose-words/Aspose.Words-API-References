---
title: "ChartLegendEntry"
linktitle: "ChartLegendEntry"
second_title: "Aspose.Words для Java"
description: "Представляет запись легенды диаграммы в Java."
type: docs
weight: 80
url: /ru/java/com.aspose.words/chartlegendentry/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartLegendEntry implements Cloneable
```

Представляет запись легенды диаграммы.

Чтобы узнать больше, посетите статью документации [ Working with Charts ][Working with Charts].

 **Remarks:** 

Запись легенды соответствует конкретному ряду диаграммы или линии тренда.

Текст записи является именем ряда или линии тренда. Текст нельзя изменить.

 **Examples:** 

Показывает, как работать со шрифтом легенды.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 ChartLegend chartLegend = chart.getLegend();
 // Set default font size all legend entries.
 chartLegend.getFont().setSize(14.0);
 // Change font for specific legend entry.
 chartLegend.getLegendEntries().get(1).getFont().setItalic(true);
 chartLegend.getLegendEntries().get(1).getFont().setSize(12.0);
 // Get legend entry for chart series.
 ChartLegendEntry legendEntry = chart.getSeries().get(0).getLegendEntry();

 doc.save(getArtifactsDir() + "Charts.LegendFont.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Методы

| Метод | Описание |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | Обеспечивает доступ к форматированию шрифта этой записи легенды. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [isHidden()](#isHidden) | Возвращает значение, указывающее, скрыта ли эта запись в легенде диаграммы. |
| [isHidden(boolean value)](#isHidden-boolean) | Устанавливает значение, указывающее, скрыта ли эта запись в легенде диаграммы. |
### fetchSpecialDefaultRunPropertyValue(int key) {#fetchSpecialDefaultRunPropertyValue-int}
```
public Object fetchSpecialDefaultRunPropertyValue(int key)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |

**Returns:**
java.lang.Object
### generateItemText() {#generateItemText}
```
public String generateItemText()
```




**Returns:**
java.lang.String
### getFont() {#getFont}
```
public Font getFont()
```


Обеспечивает доступ к форматированию шрифта этой записи легенды.

 **Examples:** 

Показывает, как работать со шрифтом легенды.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 ChartLegend chartLegend = chart.getLegend();
 // Set default font size all legend entries.
 chartLegend.getFont().setSize(14.0);
 // Change font for specific legend entry.
 chartLegend.getLegendEntries().get(1).getFont().setItalic(true);
 chartLegend.getLegendEntries().get(1).getFont().setSize(12.0);
 // Get legend entry for chart series.
 ChartLegendEntry legendEntry = chart.getSeries().get(0).getLegendEntry();

 doc.save(getArtifactsDir() + "Charts.LegendFont.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getRelativePropertyValue(int key, Object value) {#getRelativePropertyValue-int-java.lang.Object}
```
public Object getRelativePropertyValue(int key, Object value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |
| значение | java.lang.Object |  |

**Returns:**
java.lang.Object
### isHidden() {#isHidden}
```
public boolean isHidden()
```


Возвращает значение, указывающее, скрыта ли эта запись в легенде диаграммы. Значение по умолчанию — **false**.

 **Remarks:** 

Когда запись легенды диаграммы скрыта, это не влияет на соответствующий ряд или линию тренда, которые продолжают отображаться на диаграмме.

 **Examples:** 

Показывает, как работать с элементом легенды для рядов диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "AW Category 1", "AW Category 2" };

 ChartSeries series1 = series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });
 series.add("Series 3", categories, new double[] { 5.0, 6.0 });
 series.add("Series 4", categories, new double[] { 0.0, 0.0 });

 ChartLegendEntryCollection legendEntries = chart.getLegend().getLegendEntries();
 legendEntries.get(3).isHidden(true);

 doc.save(getArtifactsDir() + "Charts.LegendEntries.docx");
 
```

**Returns:**
boolean — Значение, указывающее, скрыта ли эта запись в легенде диаграммы.
### isHidden(boolean value) {#isHidden-boolean}
```
public void isHidden(boolean value)
```


Устанавливает значение, указывающее, скрыта ли эта запись в легенде диаграммы. Значение по умолчанию — **false**.

 **Remarks:** 

Когда запись легенды диаграммы скрыта, это не влияет на соответствующий ряд или линию тренда, которые продолжают отображаться на диаграмме.

 **Examples:** 

Показывает, как работать с элементом легенды для рядов диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "AW Category 1", "AW Category 2" };

 ChartSeries series1 = series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });
 series.add("Series 3", categories, new double[] { 5.0, 6.0 });
 series.add("Series 4", categories, new double[] { 0.0, 0.0 });

 ChartLegendEntryCollection legendEntries = chart.getLegend().getLegendEntries();
 legendEntries.get(3).isHidden(true);

 doc.save(getArtifactsDir() + "Charts.LegendEntries.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, указывающее, скрыта ли эта запись в легенде диаграммы. |


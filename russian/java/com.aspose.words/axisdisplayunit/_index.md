---
title: "AxisDisplayUnit"
linktitle: "AxisDisplayUnit"
second_title: "Aspose.Words для Java"
description: "Предоставляет доступ к параметрам масштабирования единиц отображения для оси значений в Java."
type: docs
weight: 26
url: /ru/java/com.aspose.words/axisdisplayunit/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class AxisDisplayUnit implements Cloneable
```

Предоставляет доступ к параметрам масштабирования единиц отображения для оси значений.

Чтобы узнать больше, посетите статью документации [ Working with Charts ][Working with Charts].

 **Examples:** 

Показывает, как управлять метками делений и отображаемыми значениями оси диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.getTickLabels().setAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabels().getSpacing());
 Assert.assertEquals(doc, axis.getDisplayUnit().getDocument());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Методы

| Метод | Описание |
| --- | --- |
| [getCustomUnit()](#getCustomUnit) | Получает пользовательский делитель для масштабирования единиц отображения на оси значений. |
| [getDefaultDisplayedFontSize()](#getDefaultDisplayedFontSize) |  |
| [getDefaultFontSize()](#getDefaultFontSize) |  |
| [getDefaultTitleText()](#getDefaultTitleText) |  |
| [getDocument()](#getDocument) | Возвращает документ, содержащий родительскую диаграмму. |
| [getRelativeFontSize(int chartFontSize)](#getRelativeFontSize-int) |  |
| [getStyleItem()](#getStyleItem) |  |
| [getTitleDeleted()](#getTitleDeleted) |  |
| [getTitlePosition()](#getTitlePosition) |  |
| [getUnit()](#getUnit) | Получает значение масштабирования единиц отображения в виде одного из предопределённых значений. |
| [isVisible()](#isVisible) |  |
| [setCustomUnit(double value)](#setCustomUnit-double) | Устанавливает пользовательский делитель для масштабирования единиц отображения на оси значений. |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean) |  |
| [setUnit(int value)](#setUnit-int) | Устанавливает значение масштабирования единиц отображения в виде одного из предопределённых значений. |
### getCustomUnit() {#getCustomUnit}
```
public double getCustomUnit()
```


Получает пользовательский делитель для масштабирования единиц отображения на оси значений.

 **Remarks:** 

Свойство не поддерживается новыми диаграммами MS Office 2016. Значение по умолчанию — 1.

Установка этого свойства задаёт свойство [getUnit()](../../com.aspose.words/axisdisplayunit/\#getUnit) / [setUnit(int)](../../com.aspose.words/axisdisplayunit/\#setUnit-int) в значение [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM).

 **Examples:** 

Показывает, как управлять метками делений и отображаемыми значениями оси диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.getTickLabels().setAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabels().getSpacing());
 Assert.assertEquals(doc, axis.getDisplayUnit().getDocument());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```

**Returns:**
double — пользовательский делитель для масштабирования единиц отображения на оси значений.
### getDefaultDisplayedFontSize() {#getDefaultDisplayedFontSize}
```
public double getDefaultDisplayedFontSize()
```




**Returns:**
double
### getDefaultFontSize() {#getDefaultFontSize}
```
public double getDefaultFontSize()
```




**Returns:**
double
### getDefaultTitleText() {#getDefaultTitleText}
```
public String getDefaultTitleText()
```




**Returns:**
java.lang.String
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Возвращает документ, содержащий родительскую диаграмму.

 **Examples:** 

Показывает, как управлять метками делений и отображаемыми значениями оси диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.getTickLabels().setAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabels().getSpacing());
 Assert.assertEquals(doc, axis.getDisplayUnit().getDocument());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The document containing the parent chart.
### getRelativeFontSize(int chartFontSize) {#getRelativeFontSize-int}
```
public int getRelativeFontSize(int chartFontSize)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartFontSize | int |  |

**Returns:**
int
### getStyleItem() {#getStyleItem}
```
public int getStyleItem()
```




**Returns:**
int
### getTitleDeleted() {#getTitleDeleted}
```
public boolean getTitleDeleted()
```




**Returns:**
boolean
### getTitlePosition() {#getTitlePosition}
```
public int getTitlePosition()
```




**Returns:**
int
### getUnit() {#getUnit}
```
public int getUnit()
```


Получает значение масштабирования единиц отображения в виде одного из предопределённых значений.

 **Remarks:** 

Значение по умолчанию — [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit/\#NONE). Значения [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) и [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit/\#PERCENTAGE) недоступны в некоторых типах диаграмм; см. [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) для получения дополнительной информации.

 **Examples:** 

Показывает, как управлять метками делений и отображаемыми значениями оси диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.getTickLabels().setAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabels().getSpacing());
 Assert.assertEquals(doc, axis.getDisplayUnit().getDocument());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```

**Returns:**
int — значение масштабирования единиц отображения в виде одного из предопределённых значений. Возвращаемое значение является одной из констант [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/).
### isVisible() {#isVisible}
```
public boolean isVisible()
```




**Returns:**
boolean
### setCustomUnit(double value) {#setCustomUnit-double}
```
public void setCustomUnit(double value)
```


Устанавливает пользовательский делитель для масштабирования единиц отображения на оси значений.

 **Remarks:** 

Свойство не поддерживается новыми диаграммами MS Office 2016. Значение по умолчанию — 1.

Установка этого свойства задаёт свойство [getUnit()](../../com.aspose.words/axisdisplayunit/\#getUnit) / [setUnit(int)](../../com.aspose.words/axisdisplayunit/\#setUnit-int) в значение [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM).

 **Examples:** 

Показывает, как управлять метками делений и отображаемыми значениями оси диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.getTickLabels().setAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabels().getSpacing());
 Assert.assertEquals(doc, axis.getDisplayUnit().getDocument());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Пользовательский делитель для масштабирования единиц отображения на оси значений. |

### setTitleDeleted(boolean value) {#setTitleDeleted-boolean}
```
public void setTitleDeleted(boolean value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean |  |

### setUnit(int value) {#setUnit-int}
```
public void setUnit(int value)
```


Устанавливает значение масштабирования единиц отображения в виде одного из предопределённых значений.

 **Remarks:** 

Значение по умолчанию — [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit/\#NONE). Значения [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) и [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit/\#PERCENTAGE) недоступны в некоторых типах диаграмм; см. [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) для получения дополнительной информации.

 **Examples:** 

Показывает, как управлять метками делений и отображаемыми значениями оси диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.getTickLabels().setAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabels().getSpacing());
 Assert.assertEquals(doc, axis.getDisplayUnit().getDocument());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Значение масштабирования единиц отображения в виде одного из предопределённых значений. Значение должно быть одной из констант [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/). |


---
title: "AxisDisplayUnit"
linktitle: "AxisDisplayUnit"
second_title: "Aspose.Words per Java"
description: "Fornisce l'accesso alle opzioni di scala delle unità di visualizzazione per l'asse dei valori in Java."
type: docs
weight: 26
url: /it/java/com.aspose.words/axisdisplayunit/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class AxisDisplayUnit implements Cloneable
```

Fornisce l'accesso alle opzioni di scala delle unità di visualizzazione per l'asse dei valori.

Per saperne di più, visita l'articolo di documentazione [ Working with Charts ][Working with Charts].

 **Examples:** 

Mostra come manipolare i segni di graduazione e i valori visualizzati di un asse del grafico.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getCustomUnit()](#getCustomUnit) | Ottiene un divisore definito dall'utente per scalare le unità di visualizzazione sull'asse dei valori. |
| [getDefaultDisplayedFontSize()](#getDefaultDisplayedFontSize) |  |
| [getDefaultFontSize()](#getDefaultFontSize) |  |
| [getDefaultTitleText()](#getDefaultTitleText) |  |
| [getDocument()](#getDocument) | Restituisce il documento che contiene il grafico principale. |
| [getRelativeFontSize(int chartFontSize)](#getRelativeFontSize-int) |  |
| [getStyleItem()](#getStyleItem) |  |
| [getTitleDeleted()](#getTitleDeleted) |  |
| [getTitlePosition()](#getTitlePosition) |  |
| [getUnit()](#getUnit) | Ottiene il valore di scala delle unità di visualizzazione come uno dei valori predefiniti. |
| [isVisible()](#isVisible) |  |
| [setCustomUnit(double value)](#setCustomUnit-double) | Imposta un divisore definito dall'utente per scalare le unità di visualizzazione sull'asse dei valori. |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean) |  |
| [setUnit(int value)](#setUnit-int) | Imposta il valore di scala delle unità di visualizzazione come uno dei valori predefiniti. |
### getCustomUnit() {#getCustomUnit}
```
public double getCustomUnit()
```


Ottiene un divisore definito dall'utente per scalare le unità di visualizzazione sull'asse dei valori.

 **Remarks:** 

La proprietà non è supportata dai nuovi grafici di MS Office 2016. Il valore predefinito è 1.

Impostando questa proprietà imposta la proprietà [getUnit()](../../com.aspose.words/axisdisplayunit/\#getUnit) / [setUnit(int)](../../com.aspose.words/axisdisplayunit/\#setUnit-int) a [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM).

 **Examples:** 

Mostra come manipolare i segni di graduazione e i valori visualizzati di un asse del grafico.

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
double - Un divisore definito dall'utente per scalare le unità di visualizzazione sull'asse dei valori.
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


Restituisce il documento che contiene il grafico principale.

 **Examples:** 

Mostra come manipolare i segni di graduazione e i valori visualizzati di un asse del grafico.

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
| Parametro | Tipo | Descrizione |
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


Ottiene il valore di scala delle unità di visualizzazione come uno dei valori predefiniti.

 **Remarks:** 

Il valore predefinito è [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit/\#NONE). I valori [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) e [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit/\#PERCENTAGE) non sono disponibili in alcuni tipi di grafico; vedere [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) per ulteriori informazioni.

 **Examples:** 

Mostra come manipolare i segni di graduazione e i valori visualizzati di un asse del grafico.

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
int - Il valore di scala delle unità di visualizzazione come uno dei valori predefiniti. Il valore restituito è una delle costanti [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/).
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


Imposta un divisore definito dall'utente per scalare le unità di visualizzazione sull'asse dei valori.

 **Remarks:** 

La proprietà non è supportata dai nuovi grafici di MS Office 2016. Il valore predefinito è 1.

Impostando questa proprietà imposta la proprietà [getUnit()](../../com.aspose.words/axisdisplayunit/\#getUnit) / [setUnit(int)](../../com.aspose.words/axisdisplayunit/\#setUnit-int) a [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM).

 **Examples:** 

Mostra come manipolare i segni di graduazione e i valori visualizzati di un asse del grafico.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | Un divisore definito dall'utente per scalare le unità di visualizzazione sull'asse dei valori. |

### setTitleDeleted(boolean value) {#setTitleDeleted-boolean}
```
public void setTitleDeleted(boolean value)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean |  |

### setUnit(int value) {#setUnit-int}
```
public void setUnit(int value)
```


Imposta il valore di scala delle unità di visualizzazione come uno dei valori predefiniti.

 **Remarks:** 

Il valore predefinito è [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit/\#NONE). I valori [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) e [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit/\#PERCENTAGE) non sono disponibili in alcuni tipi di grafico; vedere [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) per ulteriori informazioni.

 **Examples:** 

Mostra come manipolare i segni di graduazione e i valori visualizzati di un asse del grafico.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore di scala delle unità di visualizzazione come uno dei valori predefiniti. Il valore deve essere una delle costanti [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/). |


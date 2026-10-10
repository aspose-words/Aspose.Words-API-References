---
title: "ChartXValueCollection"
linktitle: "ChartXValueCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de valores X para una serie de gráfico en Java."
type: docs
weight: 95
url: /es/java/com.aspose.words/chartxvaluecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartXValueCollection implements Iterable
```

Representa una colección de valores X para una serie de gráfico.

 **Remarks:** 

Todos los elementos de la colección, excepto **null**, deben tener el mismo [ChartXValue.getValueType()](../../com.aspose.words/chartxvalue/\#getValueType).

La colección solo permite cambiar valores X. Para agregar o insertar nuevos valores a una serie de gráfico, o eliminar valores, se pueden usar los métodos apropiados de la clase [ChartSeries](../../com.aspose.words/chartseries/).

 **Examples:** 

Muestra cómo obtener los datos de la serie de gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series = chart.getSeries().get(0);

 double minValue = Double.MAX_VALUE;
 int minValueIndex = 0;
 double maxValue = -Double.MAX_VALUE;
 int maxValueIndex = 0;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     // Clear individual format of all data points.
     // Data points and data values are one-to-one in column charts.
     series.getDataPoints().get(i).clearFormat();

     // Get Y value.
     double yValue = series.getYValues().get(i).getDoubleValue();

     if (yValue < minValue)
     {
         minValue = yValue;
         minValueIndex = i;
     }

     if (yValue > maxValue)
     {
         maxValue = yValue;
         maxValueIndex = i;
     }
 }

 // Change colors of the max and min values.
 series.getDataPoints().get(minValueIndex).getFormat().getFill().setForeColor(Color.RED);
 series.getDataPoints().get(maxValueIndex).getFormat().getFill().setForeColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Charts.GetChartSeriesData.docx");
 
```
## Métodos

| Método | Descripción |
| --- | --- |
| [get(int index)](#get-int) | Obtiene el valor X en el índice especificado. |
| [getCount()](#getCount) | Obtiene el número de elementos en esta colección. |
| [getFormatCode()](#getFormatCode) | Obtiene el código de formato aplicado a los valores X. |
| [iterator()](#iterator) | Devuelve un objeto enumerador. |
| [set(int index, ChartXValue value)](#set-int-com.aspose.words.ChartXValue) | Establece el valor X en el índice especificado. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Establece el código de formato aplicado a los valores X. |
### get(int index) {#get-int}
```
public ChartXValue get(int index)
```


Obtiene el valor X en el índice especificado.

 **Remarks:** 

Los valores vacíos se representan como **null**.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/) - The X value at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de elementos en esta colección.

**Returns:**
int - El número de elementos en esta colección.
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


Obtiene el código de formato aplicado a los valores X.

 **Remarks:** 

El formato de número se usa para cambiar la forma en que los valores aparecen en el gráfico. Los ejemplos de formatos numéricos:

Número - "\#,\#\#0.00"

Moneda - "\\"$\\"\#,\#\#0.00"

Hora - "[$-x-systime]h:mm:ss AM/PM"

Fecha - "d/mm/yyyy"

Porcentaje - "0.00%"

Fracción - "\# ?/?"

Científico - "0.00E+00"

Contabilidad - "\_-\\\"$\\\"\* \#,\#\#0.00\_-;-\\\"$\\\"\* \#,\#\#0.00\_-;\_-\\\"$\\\"\* \\\"-\\\"??\_-;\_-@\_-"

Personalizado con color - "[Red]-\#,\#\#0.0"

 **Examples:** 

Muestra cómo trabajar con el código de formato de los datos del gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Returns:**
java.lang.String - El código de formato aplicado a los valores X.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto enumerador.

**Returns:**
java.util.Iterator
### set(int index, ChartXValue value) {#set-int-com.aspose.words.ChartXValue}
```
public void set(int index, ChartXValue value)
```


Establece el valor X en el índice especificado.

 **Remarks:** 

Los valores vacíos se representan como **null**.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |
| value | [ChartXValue](../../com.aspose.words/chartxvalue/) | El valor X en el índice especificado. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Establece el código de formato aplicado a los valores X.

 **Remarks:** 

El formato de número se usa para cambiar la forma en que los valores aparecen en el gráfico. Los ejemplos de formatos numéricos:

Número - "\#,\#\#0.00"

Moneda - "\\"$\\"\#,\#\#0.00"

Hora - "[$-x-systime]h:mm:ss AM/PM"

Fecha - "d/mm/yyyy"

Porcentaje - "0.00%"

Fracción - "\# ?/?"

Científico - "0.00E+00"

Contabilidad - "\_-\\\"$\\\"\* \#,\#\#0.00\_-;-\\\"$\\\"\* \#,\#\#0.00\_-;\_-\\\"$\\\"\* \\\"-\\\"??\_-;\_-@\_-"

Personalizado con color - "[Red]-\#,\#\#0.0"

 **Examples:** 

Muestra cómo trabajar con el código de formato de los datos del gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El código de formato aplicado a los valores X. |


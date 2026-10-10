---
title: "BubbleSizeCollection"
linktitle: "BubbleSizeCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de tamaños de burbujas para una serie de gráfico en Java."
type: docs
weight: 50
url: /es/java/com.aspose.words/bubblesizecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BubbleSizeCollection implements Iterable
```

Representa una colección de tamaños de burbuja para una serie de gráfico.

 **Remarks:** 

La colección solo permite cambiar los tamaños de burbujas. Para agregar o insertar nuevos valores a una serie de gráfico, o eliminar valores, se pueden usar los métodos apropiados de la clase [ChartSeries](../../com.aspose.words/chartseries/).

Los valores vacíos de tamaño de burbuja se representan como double\#NA\_N.NA\_N.
## Métodos

| Método | Descripción |
| --- | --- |
| [get(int index)](#get-int) | Obtiene el valor del tamaño de la burbuja en el índice especificado. |
| [getCount()](#getCount) | Obtiene el número de elementos en esta colección. |
| [getFormatCode()](#getFormatCode) | Obtiene el código de formato aplicado a los tamaños de burbujas. |
| [iterator()](#iterator) | Devuelve un objeto enumerador. |
| [set(int index, double value)](#set-int-double) | Establece el valor del tamaño de la burbuja en el índice especificado. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Establece el código de formato aplicado a los tamaños de burbujas. |
### get(int index) {#get-int}
```
public double get(int index)
```


Obtiene el valor del tamaño de la burbuja en el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
double - El valor del tamaño de la burbuja en el índice especificado.
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


Obtiene el código de formato aplicado a los tamaños de burbujas.

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
java.lang.String - El código de formato aplicado a los tamaños de burbujas.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto enumerador.

**Returns:**
java.util.Iterator
### set(int index, double value) {#set-int-double}
```
public void set(int index, double value)
```


Establece el valor del tamaño de la burbuja en el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |
| valor | double | El valor del tamaño de la burbuja en el índice especificado. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Establece el código de formato aplicado a los tamaños de burbujas.

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
| valor | java.lang.String | El código de formato aplicado a los tamaños de burbujas. |


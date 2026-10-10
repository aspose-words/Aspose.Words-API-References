---
title: "ChartYValue"
linktitle: "ChartYValue"
second_title: "Aspose.Words para Java"
description: "Representa un valor Y para una serie de gráfico en Java."
type: docs
weight: 97
url: /es/java/com.aspose.words/chartyvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartYValue
```

Representa un valor Y para una serie de gráfico.

 **Remarks:** 

Esta clase contiene varios métodos estáticos para crear un valor Y de un tipo particular. La propiedad [getValueType()](../../com.aspose.words/chartyvalue/\#getValueType) le permite determinar el tipo de un valor Y existente.

Todos los valores Y no nulos de una serie de gráfico deben ser del mismo tipo [ChartYValueType](../../com.aspose.words/chartyvaluetype/).
## Métodos

| Método | Descripción |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Obtiene una bandera que indica si el objeto especificado es igual al objeto de valor Y actual. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Crea una instancia de [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | Crea una instancia de [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Crea una instancia de [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | Obtiene el valor datetime almacenado. |
| [getDoubleValue()](#getDoubleValue) | Obtiene el valor numérico almacenado. |
| [getTimeValue()](#getTimeValue) | Obtiene el valor de tiempo almacenado. |
| [getValueType()](#getValueType) | Obtiene el tipo del valor Y almacenado en el objeto. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Obtiene una bandera que indica si el objeto especificado es igual al objeto de valor Y actual.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartYValue fromDateTime(Date value)
```


Crea una instancia de [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.util.Date |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartYValue fromDouble(double value)
```


Crea una instancia de [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE).

 **Examples:** 

Muestra cómo rellenar series de gráficos con datos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | double |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartYValue fromTimeSpan(long value)
```


Crea una instancia de [ChartYValue](../../com.aspose.words/chartyvalue/) del tipo [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | long |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### getDateTimeValue() {#getDateTimeValue}
```
public Date getDateTimeValue()
```


Obtiene el valor datetime almacenado.

**Returns:**
java.util.Date - El valor de fecha y hora almacenado.
### getDoubleValue() {#getDoubleValue}
```
public double getDoubleValue()
```


Obtiene el valor numérico almacenado.

**Returns:**
double - El valor numérico almacenado.
### getTimeValue() {#getTimeValue}
```
public long getTimeValue()
```


Obtiene el valor de tiempo almacenado.

**Returns:**
long - El valor de tiempo almacenado.
### getValueType() {#getValueType}
```
public int getValueType()
```


Obtiene el tipo del valor Y almacenado en el objeto.

**Returns:**
int - El tipo del valor Y almacenado en el objeto. El valor devuelto es una de las constantes de [ChartYValueType](../../com.aspose.words/chartyvaluetype/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int

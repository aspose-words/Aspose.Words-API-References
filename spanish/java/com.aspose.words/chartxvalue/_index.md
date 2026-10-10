---
title: "ChartXValue"
linktitle: "ChartXValue"
second_title: "Aspose.Words para Java"
description: "Representa un valor X para una serie de gráfico en Java."
type: docs
weight: 94
url: /es/java/com.aspose.words/chartxvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartXValue
```

Representa un valor X para una serie de gráfico.

 **Remarks:** 

Esta clase contiene varios métodos estáticos para crear un valor X de un tipo particular. La propiedad [getValueType()](../../com.aspose.words/chartxvalue/\#getValueType) le permite determinar el tipo de un valor X existente.

Todos los valores X no nulos de una serie de gráfico deben ser del mismo tipo [ChartXValueType](../../com.aspose.words/chartxvaluetype/).

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
## Métodos

| Método | Descripción |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Obtiene una bandera que indica si el objeto especificado es igual al objeto de valor X actual. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Crea una instancia de [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | Crea una instancia de [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE). |
| [fromMultilevelValue(ChartMultilevelValue value)](#fromMultilevelValue-com.aspose.words.ChartMultilevelValue) | Crea una instancia de [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL). |
| [fromString(String value)](#fromString-java.lang.String) | Crea una instancia de [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Crea una instancia de [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | Obtiene el valor datetime almacenado. |
| [getDoubleValue()](#getDoubleValue) | Obtiene el valor numérico almacenado. |
| [getMultilevelValue()](#getMultilevelValue) | Obtiene el valor multilevel almacenado. |
| [getStringValue()](#getStringValue) | Obtiene el valor de cadena almacenado. |
| [getTimeValue()](#getTimeValue) | Obtiene el valor de tiempo almacenado. |
| [getValueType()](#getValueType) | Obtiene el tipo del valor X almacenado en el objeto. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Obtiene una bandera que indica si el objeto especificado es igual al objeto de valor X actual.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartXValue fromDateTime(Date value)
```


Crea una instancia de [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.util.Date |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartXValue fromDouble(double value)
```


Crea una instancia de [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE).

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
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromMultilevelValue(ChartMultilevelValue value) {#fromMultilevelValue-com.aspose.words.ChartMultilevelValue}
```
public static ChartXValue fromMultilevelValue(ChartMultilevelValue value)
```


Crea una instancia de [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromString(String value) {#fromString-java.lang.String}
```
public static ChartXValue fromString(String value)
```


Crea una instancia de [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING).

 **Examples:** 

Muestra cómo agregar/quitar valores de datos del gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries department1Series = chart.getSeries().get(0);
 ChartSeries department2Series = chart.getSeries().get(1);

 // Remove the first value in the both series.
 department1Series.remove(0);
 department2Series.remove(0);

 // Add new values to the both series.
 ChartXValue newXCategory = ChartXValue.fromString("Q1, 2023");
 department1Series.add(newXCategory, ChartYValue.fromDouble(10.3));
 department2Series.add(newXCategory, ChartYValue.fromDouble(5.7));

 doc.save(getArtifactsDir() + "Charts.ChartDataValues.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartXValue fromTimeSpan(long value)
```


Crea una instancia de [ChartXValue](../../com.aspose.words/chartxvalue/) del tipo [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | long |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
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
### getMultilevelValue() {#getMultilevelValue}
```
public ChartMultilevelValue getMultilevelValue()
```


Obtiene el valor multilevel almacenado.

**Returns:**
[ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) - The stored multilevel value.
### getStringValue() {#getStringValue}
```
public String getStringValue()
```


Obtiene el valor de cadena almacenado.

**Returns:**
java.lang.String - El valor de cadena almacenado.
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


Obtiene el tipo del valor X almacenado en el objeto.

**Returns:**
int - El tipo del valor X almacenado en el objeto. El valor devuelto es una de las constantes de [ChartXValueType](../../com.aspose.words/chartxvaluetype/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int

---
title: "ChartNumberFormat"
linktitle: "ChartNumberFormat"
second_title: "Aspose.Words para Java"
description: "Representa el formato numérico del elemento padre en Java."
type: docs
weight: 84
url: /es/java/com.aspose.words/chartnumberformat/
---

**Inheritance:**
java.lang.Object
```
public class ChartNumberFormat
```

Representa el formato numérico del elemento padre.

Para obtener más información, visite el artículo de documentación [ Working with Charts ][Working with Charts].

 **Examples:** 

Muestra cómo establecer el formato para los valores del gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Métodos

| Método | Descripción |
| --- | --- |
| [getFormatCode()](#getFormatCode) | Obtiene el código de formato aplicado a una etiqueta de datos. |
| [isLinkedToSource()](#isLinkedToSource) | Especifica si el código de formato está vinculado a una celda de origen. |
| [isLinkedToSource(boolean value)](#isLinkedToSource-boolean) | Especifica si el código de formato está vinculado a una celda de origen. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Establece el código de formato aplicado a una etiqueta de datos. |
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


Obtiene el código de formato aplicado a una etiqueta de datos.

 **Remarks:** 

El formato numérico se utiliza para cambiar la forma en que un valor aparece en la etiqueta de datos y puede usarse de maneras muy creativas. Los ejemplos de formatos numéricos:

Número - "\#,\#\#0.00"

Moneda - "\\"$\\"\#,\#\#0.00"

Hora - "[$-x-systime]h:mm:ss AM/PM"

Fecha - "d/mm/yyyy"

Porcentaje - "0.00%"

Fracción - "\# ?/?"

Científico - "0.00E+00"

Texto - \"@\"

Contabilidad - "\_-\\\"$\\\"\* \#,\#\#0.00\_-;-\\\"$\\\"\* \#,\#\#0.00\_-;\_-\\\"$\\\"\* \\\"-\\\"??\_-;\_-@\_-"

Personalizado con color - "[Red]-\#,\#\#0.0"

 **Examples:** 

Muestra cómo habilitar y configurar etiquetas de datos para una serie de gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a line chart, then clear its demo data series to start with a clean chart,
 // and then set a title.
 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();
 chart.getSeries().clear();
 chart.getTitle().setText("Monthly sales report");

 // Insert a custom chart series with months as categories for the X-axis,
 // and respective decimal amounts for the Y-axis.
 ChartSeries series = chart.getSeries().add("Revenue",
         new String[]{"January", "February", "March"},
         new double[]{25.611d, 21.439d, 33.750d});

 // Enable data labels, and then apply a custom number format for values displayed in the data labels.
 // This format will treat displayed decimal values as millions of US Dollars.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getNumberFormat().setFormatCode("\"US$\" #,##0.000\"M\"");
 dataLabels.getFont().setSize(12.0);

 doc.save(getArtifactsDir() + "Charts.DataLabelNumberFormat.docx");
 
```

Muestra cómo establecer el formato para los valores del gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```

**Returns:**
java.lang.String - El código de formato aplicado a una etiqueta de datos.
### isLinkedToSource() {#isLinkedToSource}
```
public boolean isLinkedToSource()
```


Especifica si el código de formato está vinculado a una celda de origen. El valor predeterminado es true.

 **Remarks:** 

El NumberFormat se restablecerá a general si el código de formato está vinculado al origen.

 **Examples:** 

Muestra cómo establecer el formato para los valores del gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### isLinkedToSource(boolean value) {#isLinkedToSource-boolean}
```
public void isLinkedToSource(boolean value)
```


Especifica si el código de formato está vinculado a una celda de origen. El valor predeterminado es true.

 **Remarks:** 

El NumberFormat se restablecerá a general si el código de formato está vinculado al origen.

 **Examples:** 

Muestra cómo establecer el formato para los valores del gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Establece el código de formato aplicado a una etiqueta de datos.

 **Remarks:** 

El formato numérico se utiliza para cambiar la forma en que un valor aparece en la etiqueta de datos y puede usarse de maneras muy creativas. Los ejemplos de formatos numéricos:

Número - "\#,\#\#0.00"

Moneda - "\\"$\\"\#,\#\#0.00"

Hora - "[$-x-systime]h:mm:ss AM/PM"

Fecha - "d/mm/yyyy"

Porcentaje - "0.00%"

Fracción - "\# ?/?"

Científico - "0.00E+00"

Texto - \"@\"

Contabilidad - "\_-\\\"$\\\"\* \#,\#\#0.00\_-;-\\\"$\\\"\* \#,\#\#0.00\_-;\_-\\\"$\\\"\* \\\"-\\\"??\_-;\_-@\_-"

Personalizado con color - "[Red]-\#,\#\#0.0"

 **Examples:** 

Muestra cómo habilitar y configurar etiquetas de datos para una serie de gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a line chart, then clear its demo data series to start with a clean chart,
 // and then set a title.
 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();
 chart.getSeries().clear();
 chart.getTitle().setText("Monthly sales report");

 // Insert a custom chart series with months as categories for the X-axis,
 // and respective decimal amounts for the Y-axis.
 ChartSeries series = chart.getSeries().add("Revenue",
         new String[]{"January", "February", "March"},
         new double[]{25.611d, 21.439d, 33.750d});

 // Enable data labels, and then apply a custom number format for values displayed in the data labels.
 // This format will treat displayed decimal values as millions of US Dollars.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getNumberFormat().setFormatCode("\"US$\" #,##0.000\"M\"");
 dataLabels.getFont().setSize(12.0);

 doc.save(getArtifactsDir() + "Charts.DataLabelNumberFormat.docx");
 
```

Muestra cómo establecer el formato para los valores del gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El código de formato aplicado a una etiqueta de datos. |


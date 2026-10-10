---
title: "ChartNumberFormat"
linktitle: "ChartNumberFormat"
second_title: "Aspose.Words für Java"
description: "Stellt die Zahlenformatierung des übergeordneten Elements in Java dar."
type: docs
weight: 84
url: /de/java/com.aspose.words/chartnumberformat/
---

**Inheritance:**
java.lang.Object
```
public class ChartNumberFormat
```

Stellt die Zahlenformatierung des übergeordneten Elements dar.

Weitere Informationen finden Sie im Dokumentationsartikel zu [ Working with Charts ][Working with Charts].

 **Examples:** 

Zeigt, wie man die Formatierung für Diagrammwerte festlegt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getFormatCode()](#getFormatCode) | Ruft den auf eine Datenbeschriftung angewendeten Formatcode ab. |
| [isLinkedToSource()](#isLinkedToSource) | Gibt an, ob der Formatcode mit einer Quellzelle verknüpft ist. |
| [isLinkedToSource(boolean value)](#isLinkedToSource-boolean) | Gibt an, ob der Formatcode mit einer Quellzelle verknüpft ist. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Setzt den auf eine Datenbeschriftung angewendeten Formatcode. |
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


Ruft den auf eine Datenbeschriftung angewendeten Formatcode ab.

 **Remarks:** 

Zahlenformatierung wird verwendet, um die Darstellung eines Wertes in einer Datenbeschriftung zu ändern und kann auf sehr kreative Weise eingesetzt werden. Beispiele für Zahlenformate:

Zahl - "\\#,\\#\\#0.00"

Währung - "\\"$\\"\#,\#\#0.00"

Zeit - "[$-x-systime]h:mm:ss AM/PM"

Datum - "d/mm/yyyy"

Prozent - "0.00%"

Bruch - "\# ?/?"

Wissenschaftlich - "0.00E+00"

Text - "@"

Buchhaltung - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Benutzerdefiniert mit Farbe - "[Red]-\#,\#\#0.0"

 **Examples:** 

Zeigt, wie man Datenbeschriftungen für eine Diagrammserie aktiviert und konfiguriert.

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

Zeigt, wie man die Formatierung für Diagrammwerte festlegt.

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
java.lang.String - Der auf eine Datenbeschriftung angewendete Formatcode.
### isLinkedToSource() {#isLinkedToSource}
```
public boolean isLinkedToSource()
```


Gibt an, ob der Formatcode mit einer Quellzelle verknüpft ist. Standard ist true.

 **Remarks:** 

Das NumberFormat wird auf allgemein zurückgesetzt, wenn der Formatcode mit der Quelle verknüpft ist.

 **Examples:** 

Zeigt, wie man die Formatierung für Diagrammwerte festlegt.

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
boolean - Der entsprechende  boolean  Wert.
### isLinkedToSource(boolean value) {#isLinkedToSource-boolean}
```
public void isLinkedToSource(boolean value)
```


Gibt an, ob der Formatcode mit einer Quellzelle verknüpft ist. Standard ist true.

 **Remarks:** 

Das NumberFormat wird auf allgemein zurückgesetzt, wenn der Formatcode mit der Quelle verknüpft ist.

 **Examples:** 

Zeigt, wie man die Formatierung für Diagrammwerte festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Setzt den auf eine Datenbeschriftung angewendeten Formatcode.

 **Remarks:** 

Zahlenformatierung wird verwendet, um die Darstellung eines Wertes in einer Datenbeschriftung zu ändern und kann auf sehr kreative Weise eingesetzt werden. Beispiele für Zahlenformate:

Zahl - "\\#,\\#\\#0.00"

Währung - "\\"$\\"\#,\#\#0.00"

Zeit - "[$-x-systime]h:mm:ss AM/PM"

Datum - "d/mm/yyyy"

Prozent - "0.00%"

Bruch - "\# ?/?"

Wissenschaftlich - "0.00E+00"

Text - "@"

Buchhaltung - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Benutzerdefiniert mit Farbe - "[Red]-\#,\#\#0.0"

 **Examples:** 

Zeigt, wie man Datenbeschriftungen für eine Diagrammserie aktiviert und konfiguriert.

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

Zeigt, wie man die Formatierung für Diagrammwerte festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der auf eine Datenbeschriftung angewendete Formatcode. |


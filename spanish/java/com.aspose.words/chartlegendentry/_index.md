---
title: "ChartLegendEntry"
linktitle: "ChartLegendEntry"
second_title: "Aspose.Words para Java"
description: "Representa una entrada de leyenda de gráfico en Java."
type: docs
weight: 80
url: /es/java/com.aspose.words/chartlegendentry/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartLegendEntry implements Cloneable
```

Representa una entrada de la leyenda del gráfico.

Para obtener más información, visite el artículo de documentación [ Working with Charts ][Working with Charts].

 **Remarks:** 

Una entrada de leyenda corresponde a una serie de gráfico o línea de tendencia específica.

El texto de la entrada es el nombre de la serie o línea de tendencia. El texto no se puede cambiar.

 **Examples:** 

Muestra cómo trabajar con la fuente de la leyenda.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | Proporciona acceso al formato de fuente de esta entrada de leyenda. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [isHidden()](#isHidden) | Obtiene un valor que indica si esta entrada está oculta en la leyenda del gráfico. |
| [isHidden(boolean value)](#isHidden-boolean) | Establece un valor que indica si esta entrada está oculta en la leyenda del gráfico. |
### fetchSpecialDefaultRunPropertyValue(int key) {#fetchSpecialDefaultRunPropertyValue-int}
```
public Object fetchSpecialDefaultRunPropertyValue(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

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


Proporciona acceso al formato de fuente de esta entrada de leyenda.

 **Examples:** 

Muestra cómo trabajar con la fuente de la leyenda.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

**Returns:**
java.lang.Object
### isHidden() {#isHidden}
```
public boolean isHidden()
```


Obtiene un valor que indica si esta entrada está oculta en la leyenda del gráfico. El valor predeterminado es **false**.

 **Remarks:** 

Cuando una entrada de leyenda de gráfico está oculta, no afecta a la serie de gráfico o línea de tendencia correspondiente que sigue mostrada en el gráfico.

 **Examples:** 

Muestra cómo trabajar con una entrada de leyenda para series de gráficos.

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
boolean - Un valor que indica si esta entrada está oculta en la leyenda del gráfico.
### isHidden(boolean value) {#isHidden-boolean}
```
public void isHidden(boolean value)
```


Establece un valor que indica si esta entrada está oculta en la leyenda del gráfico. El valor predeterminado es **false**.

 **Remarks:** 

Cuando una entrada de leyenda de gráfico está oculta, no afecta a la serie de gráfico o línea de tendencia correspondiente que sigue mostrada en el gráfico.

 **Examples:** 

Muestra cómo trabajar con una entrada de leyenda para series de gráficos.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica si esta entrada está oculta en la leyenda del gráfico. |

